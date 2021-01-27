# -- Programmed by OmarMazin
# -- Add me on instagram @omarmazin_
import requests
import re
print('add me instagram >> @omarmazin_')
def info():
    i = input(' Enter Username >> :')
    url = 'https://www.instagram.com/'+i+'/?__a=1'
    try:
        req = requests.get(url).text
        ava = re.search(r'"profile_pic_url_hd":"(.*?)"',req).groups(1)
        print(f'Hd Avatar >>{ava}')
        use = re.search(r'"logging_page_id":"profilePage_(.*?)"', req).groups(1)
        print(f'User id >> {use}')
        name = re.search(r',"full_name":"(.*?)"' , req).groups(1)
        print(f'Full name >> {name}')
        bio = re.search(r'"show_follow_dialog":false,"graphql":{"user":{"biography":"(.*?)"',req).groups(1)
        print(f'Bio >> {bio}')
        fol = re.search(r'"edge_followed_by":{"count":(.*?)}' , req).groups(1)
        print(f'Followers >> {fol}')
        folg = re.search(r'"edge_follow":{"count":(.*?)}' , req).groups(1)
        print(f'Following >> {folg}')
        try:
            cat = re.search(r'"category_enum":null,"category_name":"(.*?)"',req).groups(1)
            print(cat)
        except:
            print('Not a Creator')
        try:
            bus = re.search(r'"business_category_name":"(.*?)":null,"category_enum":"TOPIC_SHOPPING_RETAIL","category_name":"(.*?)"' , req).groups(1)
            print(f'Business >> {bus}')
        except:
            print('Not a Business')
    except:
        print('the user is Unavailable')
        quit()
info()
