---
description: Para usar um dicionário de aplicativos com a API do Tablet PC, você deve primeiro criar um arquivo com a lista de palavras para o dicionário do aplicativo.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788135"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="410b2-103">Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="410b2-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="410b2-104">Para usar um dicionário de aplicativos com a API do Tablet PC, você deve primeiro criar um arquivo com a lista de palavras para o dicionário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="410b2-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="410b2-105">A solução mais fácil para isso é usar um arquivo de texto que contenha uma lista das palavras.</span><span class="sxs-lookup"><span data-stu-id="410b2-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="410b2-106">Quando seu aplicativo for carregado, ele lerá o arquivo de texto e criará um objeto de lista [**de palavras a**](inkwordlist-class.md) partir de uma das listas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="410b2-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="410b2-107">Para cada [**RecognizerContext**](inkrecognizercontext-class.md) associado ao dicionário do aplicativo, defina a propriedade lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto **RecognizerContext** para a lista de palavras no arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="410b2-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="410b2-108">O exemplo a seguir ilustra como criar um objeto de [**listas de palavras**](inkwordlist-class.md) de uma coleção [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="410b2-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="410b2-109">Este exemplo pressupõe que você já carregou a lista de palavras do disco e criou uma coleção StringCollection dessas palavras.</span><span class="sxs-lookup"><span data-stu-id="410b2-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> <span data-ttu-id="410b2-110">A propriedade [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) deve estar vazia antes de você definir a propriedade de [**palavras**](inkwordlist-class.md) -folha.</span><span class="sxs-lookup"><span data-stu-id="410b2-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="410b2-111">Se a propriedade [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) não estiver vazia, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="410b2-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="410b2-112">Além disso, as palavras nunca devem ser adicionadas a uma lista de palavras após serem atribuídas a um objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="410b2-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="410b2-113">As palavras que são adicionadas à lista de palavras após serem atribuídas ao objeto **RecognizerContext** não são atualizadas no reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="410b2-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="410b2-114">Para atualizar a lista de palavras, você deve reatribuir o objeto de [**folha de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) **palavras** à propriedade lista de palavras do objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="410b2-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="410b2-115">Para obter precisão máxima de reconhecimento, combine as factos com o dicionário do aplicativo em uma relação vantajosa.</span><span class="sxs-lookup"><span data-stu-id="410b2-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="410b2-116">Para obter mais informações sobre a relação entre os factos e os dicionários do aplicativo, consulte [noções básicas sobre listas de palavras, contexto do reconhecedor e factos](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="410b2-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="410b2-117">Para obter um exemplo de como usar dicionários de aplicativo com o controle [InkEdit](inkedit-control-reference.md) , consulte [usando um dicionário de aplicativo com InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="410b2-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
