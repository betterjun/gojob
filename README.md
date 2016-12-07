# gojob


func jobFunc(a, b int) int {}
func jobFunc1(a, b string) string {}
func jobFunc2(a string, b int) bool {}

var s Scheduler
s.Start(jobFunc, args...)
s.Wait()

s.StartGroup(groupName, jobFunc1, args...)
s.StartGroup(groupName, jobFunc2, args...)
s.WaitGroup(groupName)

s.WaitAll()
s.WaitAllGroup()
