---
description: Para usar um dicionário de aplicativos com a API do Tablet PC, você deve primeiro criar um arquivo com a lista de palavras para o dicionário do aplicativo.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c30fec5539a9b1f4efb0ca89a53568becff2368942d069149106a4032676d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091289"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC

Para usar um dicionário de aplicativos com a API do Tablet PC, você deve primeiro criar um arquivo com a lista de palavras para o dicionário do aplicativo.

A solução mais fácil para isso é usar um arquivo de texto que contenha uma lista das palavras. Quando seu aplicativo for carregado, ele lerá o arquivo de texto e criará um objeto de lista [**de palavras a**](inkwordlist-class.md) partir de uma das listas do arquivo. Para cada [**RecognizerContext**](inkrecognizercontext-class.md) associado ao dicionário do aplicativo, defina a propriedade lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto **RecognizerContext** para a lista de palavras no arquivo de texto.

O exemplo a seguir ilustra como criar um objeto de [**listas de palavras**](inkwordlist-class.md) de uma coleção [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) . Este exemplo pressupõe que você já carregou a lista de palavras do disco e criou uma coleção StringCollection dessas palavras.


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
> A propriedade [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) deve estar vazia antes de você definir a propriedade de [**palavras**](inkwordlist-class.md) -folha. Se a propriedade [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) não estiver vazia, uma exceção será lançada. Além disso, as palavras nunca devem ser adicionadas a uma lista de palavras após serem atribuídas a um objeto **RecognizerContext** . As palavras que são adicionadas à lista de palavras após serem atribuídas ao objeto **RecognizerContext** não são atualizadas no reconhecedor. Para atualizar a lista de palavras, você deve reatribuir o objeto de [**folha de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) **palavras** à propriedade lista de palavras do objeto **RecognizerContext** .

 

Para obter precisão máxima de reconhecimento, combine as factos com o dicionário do aplicativo em uma relação vantajosa. Para obter mais informações sobre a relação entre os factos e os dicionários do aplicativo, consulte [noções básicas sobre listas de palavras, contexto do reconhecedor e factos](understanding-wordlists--the-recognizercontext--and-factoids.md).

Para obter um exemplo de como usar dicionários de aplicativo com o controle [InkEdit](inkedit-control-reference.md) , consulte [usando um dicionário de aplicativo com InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
