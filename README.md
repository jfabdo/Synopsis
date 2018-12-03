Synopsis allows you to view a brief overview of articles and other texts on your Android phone. Future versions will include an Android APK to load on your phone which has an interface to help you.

Current versions simply sums up text inputs.

Usage is `java -jar Synopsis.jar testarticle.txt`

Ex:  
`java -jar Synopsis.jar testarticle4.txt `

> Qualcomm was dealt a major loss in one of its many ongoing legal battles this afternoon, with a federal court ruling that the company must license its modem patents to competing chipmakers, potentially weakening its stranglehold on the market.  The crux of the lawsuit — whether Qualcomm used anti-competitive practices to maintain a monopoly over smartphone modems — isn’t being ruled on here. 

API:

The class Article takes an article as input. Available variables and methods are as follows:  
  article- Contains the full article input  
  synopsis- Contains a few key sentences from the article.  
  tagcloud- Contains the top keywords from the article  

Example:
fun main(args: Array<String>) {  
  for (i in args) {  
    val inputarticle = Article(File(i).readText())  
    println(inputarticle.tagcloud)  
    println(inputarticle.summary+"\n\n\n")  
    println(inputarticle.wordscore)  
  }  
}  
