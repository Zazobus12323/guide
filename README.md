# guide
please don`t open

настройка окружения
solution(content)
const showInfo = (content) =>{
  const data = content.split('\n').slice(1).map((el) => el.split(','))
  console.log(data)
}
export default showInfo
