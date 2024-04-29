https://github.com/TommyJD93/Philosophers?tab=readme-ov-file#General_idea


## RULEZ:
◦ No global vars!
◦ Announcement of DEATH no more than 10ms delay!
◦ 1 philo = 1 thread


## ARGS:
◦ number_of_philosophers:
    The number of philosophers and also the number of forks.
◦ time_to_die (in milliseconds):
    If a philosopher didn’t start eating time_to_die milliseconds since the
    beginning of their last meal or the beginning of the simulation, they die.
◦ time_to_eat (in milliseconds):
    The time it takes for a philosopher to eat.
    During that time, they will need to hold two forks.
◦ time_to_sleep (in milliseconds):
    The time a philosopher will spend sleeping.
◦ number_of_times_each_philosopher_must_eat (optional argument):
    If all philosophers have eaten at least 
    number_of_times_each_philosopher_must_eat times, the simulation stops.
    If not specified, the simulation stops when a philosopher dies.

## OUTPUT FORMAT:
◦ timestamp_in_ms X has taken a fork
◦ timestamp_in_ms X is eating
◦ timestamp_in_ms X is sleeping
◦ timestamp_in_ms X is thinking
◦ timestamp_in_ms X died


# RESEARCH

## MUTEXs


# EXTERNAL FUNCTIONS
#include <pthread.h>

memset
printf
malloc
free
write
usleep

gettimgettimeofday(struct timeval *restrict tp, void *restrict tzp)            #include <sys/time.h>
    The time is expressed in seconds and microseconds since midnight (0 hour), January 1, 1970.

pthread_create(pthread_t *thread, const pthread_attr_t *attr, void *(*start_routine)(void *), void *arg)
    Creates a new thread of execution.

pthread_detach(pthread_t thread)
    Marks a thread for deletion.

pthread_join(pthread_t thread, void **value_ptr)
    Causes the calling thread to wait for the termination of the specified thread.

pthread_mutex_init(pthread_mutex_t *mutex, const pthread_mutexattr_t *attr)
    Initialize a mutex with specified attributes.

pthread_mutex_destroy(pthread_mutex_t *mutex)
    Destroy a mutex.

pthread_mutex_lock(pthread_mutex_t *mutex)
    Lock a mutex and block until it becomes available.

pthread_mutex_unlock(pthread_mutex_t *mutex)
    Unlock a mutex.


# STRUCTS AND INCLUDES

#include <sys/time.h>
struct timeval {
             time_t       tv_sec;   /* seconds since Jan. 1, 1970 */
             suseconds_t  tv_usec;  /* and microseconds */
     };
     
#include <pthread.h>