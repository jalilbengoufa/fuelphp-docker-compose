# fuelphp-docker-compose

### mysql config example for site 

```
return array(
        'active' => 'local',
        'local' => array( 
            'type'           => 'mysqli',
            'connection'     => array(
                'hostname'       => 'db',
                'port'           => '3306',
                'database'       => '_live',
                'username'       => 'root',
                'password'       => 'rootpassword',
                'persistent'     => false,
                'compress'       => false,
            ),
            'identifier'     => '`',
            'table_prefix'   => '',
            'charset'        => 'utf8',
            'enable_cache'   => true,
            'profiling'      => false,
            'readonly'       => false,
        ),
        'api' => array(
            'type'           => 'mysqli',
            'connection'     => array(
                'hostname'       => 'db',
                'port'           => '3306',
                'database'       => 'api_',
                'username'       => 'root',
                'password'       => 'rootpassword',
                'persistent'     => false,
                'compress'       => false,
            ),
            'identifier'     => '`',
            'table_prefix'   => '',
            'charset'        => 'utf8',
            'enable_cache'   => true,
            'profiling'      => false,
            'readonly'       => false,
        ),
    );
```

### mysql config for the api 

```
return array(
		'active' => 'local',

		'local'  => array(
			'type'         => 'mysqli',
			'connection'   => array(
				'hostname'   => 'db',
				'port'       => '3306',
				'database'   => 'api_',
				'username'   => 'root',
				'password'   => 'rootpassword',
				'persistent' => FALSE,
				'compress'   => FALSE,
			),
			'identifier'   => '`',
			'table_prefix' => '',
			'charset'      => 'utf8',
			'enable_cache' => TRUE,
			'profiling'    => FALSE,
			'readonly'     => FALSE,
		)
	);
```