# homework3
# calculate the probability that out of 30 people at a party, no one gets their own hat when they leave. (all the hats are mixed up and equally likely outcome)

###establish that there are 30 people, each having a hat
p = 1:30
###i be a counting index
i = 1
j = 0
###create a loop to run the code 1000000 times
while (i <= 1000000) {
  y = sample (p, replace = FALSE, 30)
  ###if the vectors aren't equal (difference of the components not equal to 0)
  if (all(p - y != 0)) {
    ####sum the runs that weren't equal in any components
    j = j + 1
  }
  ###increase the index by 1
  i = i + 1
}
###print the probability of no one getting their hat back out of 1000000 times
print(j / 1000000)
