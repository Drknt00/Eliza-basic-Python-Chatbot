# Eliza-basic-Python-Chatbot
#this is a very basic chatbot that simulates human conversations by asking follow up questions

eliza_response = 'What do you need?'

while True:
    s = input(eliza_response + ' ')
    if 'I need ' in s:
        your_need = s.plit('I need ')[-1]
        eliza_response = 'Why do you need' + your_need + '?'
    elif 'because' in s:
        your_cause = s.split()[-1]
        eliza_response = 'Why are you ' + your_cause + '?'

    elif s =='quit':
        break
    else:
        eliza_response = 'Can you tell me why?'
