jsonify API 추가하기
-> LLM을 통해서 주어진 데이터를 정해진 형식으로 잘 바꿔주는 것
시나리오에서 one time으로 안끝나는 경우가 많기 때문

team이 없이도 동작가능해야함. agent free 동작임. (데모용)

image_data: {base64_image_str + ocr string}

- input
. base64_image_str[] / ocr_str[] / text(optional) / llm(37b + gpt) / output json 포멧  + (system prompt는 fw에서 들고가고..)
- output
. output json string

-> ocr 여부는 flag 처리 (aidl에서)

- app input
. image_path[] / text(optional) / llm(37b + gpt) / output json 포멧  + (system prompt는 fw에서 들고가고..)


기존 api

imagetxt[] array가 필요할수도

