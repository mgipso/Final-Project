# Final-Project
twelve_years = open('12YearsaSlave.txt', 'r', encoding='utf-8')

twelve_years = twelve_years.read()
#print(twelve_years)

my_first_read_in_text = twelve_years
my_first_read_in_text.split("CHAPTER")
#print(my_first_read_in_text.split("CHAPTER"))

topof_book = my_first_read_in_text.split('sleeps')[0]
topof_book +='sleeps.'
#print(topof_book)

twelve_clean_book = topof_book.split('\n\n\n\nNARRATIVE OF SOLOMON NORTHUP.\n\n\n\n')[1]
#print(twelve_clean_book)

myReadLines = twelve_years.split('\n')
import string

twelve_years = open('../finalProject/12YearsaSlave.txt', 'r', encoding='utf-8')
all_text_three = twelve_years.readlines()
#print(all_text_three)
twelve_years.close()

file_words = open('stopwords.txt', 'r', encoding='utf-8')
stopwords = file_words.readlines()

stopwords_cleaned = []
for word in stopwords:
    clean_word = word.replace('\n','')
    stopwords_cleaned.append(clean_word)
#lines = all_text_three
#all_text_three = lines [499:8187]
#print(all_text_three)

start_index = all_text_three.index('NARRATIVE OF SOLOMON NORTHUP.\n')
end_index = all_text_three.index('my father sleeps.\n')+1
content_lines = all_text_three[start_index:end_index]

#print(type(content_lines))

cleaned_twelve = []
for line in content_lines:
    for punc in string.punctuation:
        line = line.replace(punc, '').replace('\n', '')
    cleaned_twelve.append(line)
#print(cleaned_drac)

word_counts = {}

for line in cleaned_twelve:
    words = line.lower().split()
    for word in words:
        if word in cleaned_twelve and word not in word_counts and word not in stopwords_cleaned:
            word_counts[word] = 1
            # word_counts[word] = word_counts[word] + 1
        elif word in cleaned_twelve and word in word_counts and word not in stopwords_cleaned:
            word_counts[word] = word_counts[word] + 1
        else:
            pass

#print(word_counts)

def byFreq(pair):
    return pair[1]

word_count_tuples = list(word_counts.items())
word_count_tuples.sort(key=byFreq, reverse=True)

count = 1
for word, freq in word_count_tuples[0:100]:
    print(str(count)+'.'+"In Twelve Years a Slave" + " " + "The word "+word.capitalize()+' appeared '+ str(freq) + ' time(s).')
#    count+=1

print("**********************************")

incident_girl = open('Incident', 'r', encoding='utf-8')

incident_girl = incident_girl.read()
#print(incident_girl)

myReadLines = incident_girl.split('\n')
import string

incident = open('../finalProject/Incident', 'r', encoding='utf-8')
all_text_one = incident.readlines()
#print(all_text)
incident.close()

file_words = open('stopwords.txt', 'r', encoding='utf-8')
stopwords = file_words.readlines()

stopwords_cleaned = []
for word in stopwords:
    clean_word = word.replace('\n','')
    stopwords_cleaned.append(clean_word)
#lines = all_text
#all_text = lines [253:7373]
#print(all_text)

start_index = all_text_one.index('Incidents\n')
end_index = all_text_one.index('fleecy clouds floating over a dark and troubled sea.\n')+1
content_lines = all_text_one[start_index:end_index]

#print(type(content_lines))

cleaned_incident = []
for line in content_lines:
    for punc in string.punctuation:
        line = line.replace(punc, '').replace('\n', '')
    cleaned_incident.append(line)
#print(cleaned_drac)

word_counts = {}

for line in cleaned_incident:
    words = line.lower().split()
    for word in words:
        if word in cleaned_incident and word not in word_counts and word not in stopwords_cleaned:
            word_counts[word] = 1
            # word_counts[word] = word_counts[word] + 1
        elif word in cleaned_incident and word in word_counts and word not in stopwords_cleaned:
            word_counts[word] = word_counts[word] + 1
        else:
            pass

#print(word_counts)

def byFreq(pair):
    return pair[1]

word_count_tuples = list(word_counts.items())
word_count_tuples.sort(key=byFreq, reverse=True)

count = 1
for word, freq in word_count_tuples[0:100]:
    print(str(count)+'.'+"In Incident of a Slave Girl" + " " + "The word "+word.capitalize()+' appeared '+ str(freq) + ' time(s).')
    count+=1

print("**********************************")

sojourner_truth = open('sojourner_text', 'r', encoding='utf-8')

sojourner_truth = sojourner_truth.read()
#print(sojourner_truth)

myReadLines = sojourner_truth.split('\n')
import string

sojourner_truth = open('../finalProject/Sojourner_text', 'r', encoding='utf-8')
all_text_two = sojourner_truth.readlines()
#print(all_text)
sojourner_truth.close()

file_words = open('stopwords.txt', 'r', encoding='utf-8')
stopwords = file_words.readlines()

stopwords_cleaned = []
for word in stopwords:
    clean_word = word.replace('\n','')
    stopwords_cleaned.append(clean_word)
#lines = all_text_two
#all_text = lines [348:3916]
#print(all_text)

start_index = all_text_two.index('NARRATIVE OF SOJOURNER TRUTH\n')
end_index = all_text_two.index('partake of his spirit!\n')+1
content_lines = all_text_two[start_index:end_index]

#print(type(content_lines))

cleaned_sojourner = []
for line in content_lines:
    for punc in string.punctuation:
        line = line.replace(punc, '').replace('\n', '')
    cleaned_sojourner.append(line)
#print(cleaned_drac)

word_counts = {}

for line in cleaned_incident:
    words = line.lower().split()
    for word in words:
        if word in cleaned_sojourner and word not in word_counts and word not in stopwords_cleaned:
            word_counts[word] = 1
            # word_counts[word] = word_counts[word] + 1
        elif word in cleaned_sojourner and word in word_counts and word not in stopwords_cleaned:
            word_counts[word] = word_counts[word] + 1
        else:
            pass

#print(word_counts)

def byFreq(pair):
    return pair[1]

word_count_tuples = list(word_counts.items())
word_count_tuples.sort(key=byFreq, reverse=True)

count = 1
for word, freq in word_count_tuples[0:100]:
    print(str(count)+'.'+"In the Narrative of Sojourner Truth" + " " + "The word "+word.capitalize()+' appeared '+ str(freq) + ' time(s).')
    count+=1

print("**********************************")

life_of_e = open('life_of_e.txt', 'r', encoding='utf-8')
life_of_e = life_of_e.read()
#(life_of_e)
my_fourth_read_in_text = life_of_e
my_fourth_read_in_text.split("CHAPTER")
#print(my_fourth_read_in_text.split("CHAP."))

fourth_topof_book = my_fourth_read_in_text.split('\n\nTHE END.\n\n\n\n\n\n\n\n')[0]
#print(fourth_topof_book)

life_clean_book = fourth_topof_book.split('\n\n\n\nTHE LIFE, &c.\n\n\n\n')[1]
#print(life_clean_book)

myReadLines = life_of_e.split('\n')
import string

life_of_e = open('../finalProject/life_of_e.txt', 'r', encoding='utf-8')
all_text_four = life_of_e.readlines()
#print(all_text)
life_of_e.close()

file_words = open('stopwords.txt', 'r', encoding='utf-8')
stopwords = file_words.readlines()

stopwords_cleaned = []
for word in stopwords:
    clean_word = word.replace('\n','')
    stopwords_cleaned.append(clean_word)
#lines = all_text_four
#all_text_four = lines [622:7689]
#print(all_text_four)

start_index = all_text_four.index('THE LIFE, &c.\n')
end_index = all_text_four.index('THE END.\n')+1
content_lines = all_text_four[start_index:end_index]

#print(type(content_lines))

cleaned_life_of_e = []
for line in content_lines:
    for punc in string.punctuation:
        line = line.replace(punc, '').replace('\n', '')
    cleaned_life_of_e.append(line)
#print(cleaned_drac)

word_counts = {}

for line in cleaned_life_of_e:
    words = line.lower().split()
    for word in words:
        if word in cleaned_life_of_e and word not in word_counts and word not in stopwords_cleaned:
            word_counts[word] = 1
            # word_counts[word] = word_counts[word] + 1
        elif word in cleaned_life_of_e and word in word_counts and word not in stopwords_cleaned:
            word_counts[word] = word_counts[word] + 1
        else:
            pass

#print(word_counts)

def byFreq(pair):
    return pair[1]

word_count_tuples = list(word_counts.items())
word_count_tuples.sort(key=byFreq, reverse=True)

count = 1
for word, freq in word_count_tuples[0:100]:
    print(str(count)+'.'+"In The Interesting Narrative of the Life of Olaudah Equiano" + " " +
          "The word "+word.capitalize()+' appeared '+ str(freq) + ' time(s).')
    count+=1
