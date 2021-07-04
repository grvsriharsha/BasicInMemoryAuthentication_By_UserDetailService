# InMemoryAuthentication
First run the sql files in sql folder.

The userDetailservice is replced by ImemoryDetailsManager


	InMemoryUserDetailsManager userDetailsService=new InMemoryUserDetailsManager();
		UserDetails user=User.withUsername("tom").password(bCryptPasswordEncoder().encode("cruise")).authorities("read").build();
		userDetailsService.createUser(user);

		auth.userDetailsService(userDetailsService).passwordEncoder(bCryptPasswordEncoder());
