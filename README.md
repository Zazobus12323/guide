# guide
please don`t open

настройка окружения
solution(content)
const showInfo = (content) =>{
  const data = content.split('\n').slice(1).map((el) => el.split(','))
  console.log(data)
}
export default showInfo


export default (content) => {
    const s = content.split('\n').slice(1)
    const pop = s.map((strr) => strr.slice(2, strr.length - 1).split(' | '))
    const makeHero = (arr) => {
        const hero = {race: arr[0], strength: parseInt(arr[1]), health: parseInt(arr[2]), quantity: parseInt(arr[3]), height: parseInt(arr[4]), weight: parseInt(arr[5]), price: parseInt(arr[6])}
        return hero
    }
    const heroes = pop.map((hero) => makeHero(hero))
    console.log(heroes)

    // 1
    const qual = heroes.length
    console.log(`Количество рядов: ${qual}`)

    //2
    const super_hero = (arr) => {
        const sila = arr.map((silni) => silni.strength)
        const dlina = sila.length
        for (let i = 0; i <= dlina; i++){
            const norma = parseInt(sila[i])
            const silnishi = Math.max(norma)
            return silnishi
        }
    }
        const jopa1 = heroes.find(hero => hero.strength === super_hero(heroes))
        const popka = jopa1.price * 10
    console.log(`цена за 10 сильнейших созданий: ${popka}`)

    //2.1
    const super_hero1 = (arr) => {
        const sila = arr.map((silni) => silni.strength)
        const max = Math.max(...sila);
        const second = sila.reduce((acc, c) => c === max ? acc : Math.max(acc, c));
        return second
    }
    const jopa2 = heroes.find(hero => hero.strength === super_hero1(heroes))
    const popka1 = jopa2.price * 20
    console.log(`цена за 20 вторых по силе созданий: ${popka1}`)

    //3

    const jir_hero = (arr) => {
        const sila = arr.map((silni) => silni.weight)
        const dlina = sila.length
        for (let i = 0; i <= dlina; i++){
            const norma = parseInt(sila[i])
            const silnishi = Math.max(norma)
            return silnishi
        }}
        const jopa3 = heroes.find(hero => hero.weight === jir_hero(heroes))
        const popka3 = jopa3.price * 5
    console.log(`цена за отряд самых толстых: ${popka3}`)
    
    //3.1
    const no_jir_hero = (arr) => {
        const sila = arr.map((silni) => silni.weight)
        const dlina = sila.length
        for (let i = 0; i <= dlina; i++){
            const silnishi = Math.min(...sila)
            return silnishi
        }}
        const jopa4 = heroes.find(hero => hero.weight === no_jir_hero(heroes))
        const popka4 = jopa4.price * 5
    console.log(`цена за отряд самых тонких: ${popka4}`)

    //4
    console.log('не решено')
    const sootnos = (obj) => {
        const result = obj.price / obj.strength
        return result
    }
    const aboba = heroes.map((hero) => sootnos(hero))
    const aboba2 = Math.max(aboba)


    //5
        const r5 = 10000/jopa1.price
        console.log(`Самая лучшая армия за 10000: ${r5} ${jopa1.race}`)
    

}
