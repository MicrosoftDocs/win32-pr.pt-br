---
description: Todos os dicionários de aplicativo são implementados usando o objeto de lista de palavras.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Compreendendo as listas de palavras, o contexto do reconhecedor e as chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27f15d64f353b8702695b0067f13857427fc34e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170072"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Compreendendo as listas de palavras, o contexto do reconhecedor e as chaves

Todos os dicionários de aplicativo são implementados usando o objeto de lista de [**palavras**](inkwordlist-class.md) . O objeto [**RecognizerContext**](inkrecognizercontext-class.md) gerencia o reconhecimento, em parte por meio da propriedade de folha de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) desse objeto. O objeto **RecognizerContext** passa a lista de palavras para o reconhecedor. Você pode habilitar um dicionário de aplicativo em qualquer **RecognizerContext** em seu aplicativo definindo a **propriedade de** PropertyList do objeto **RecognizerContext** . Para disponibilizar a lista de palavras para todo o aplicativo, você deve definir a propriedade lista de **palavras** de cada objeto **RecognizerContext** no aplicativo.

No nível do reconhecedor, todos os dicionários, exceto o dicionário do sistema, são implementados como listas de palavras. No entanto, o reconhecedor só pode ter uma lista de palavras ativa por vez. Isso significa que você não pode ter um dicionário de aplicativo e o dicionário do usuário ativos ao mesmo tempo. Por outro lado, o dicionário do sistema está sempre disponível, a menos que um factor esteja definido, o que desativa o dicionário do sistema.

O dicionário do usuário é a lista de palavras que o usuário adicionou ao seu Tablet PC. Se a propriedade de lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de [**RecognizerContext**](inkrecognizercontext-class.md) não estiver definida, **RecognizerContext** passará o dicionário do usuário como uma lista de palavras para o reconhecedor. No entanto, se a propriedade de lista de **palavras** do objeto **RecognizerContext** for definida, a palavra list será passada para o Recognizer em vez do dicionário do usuário.

> [!Note]  
> A propriedade [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) deve estar vazia antes de você definir a propriedade de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -folha. Se a propriedade **Strokes** não estiver vazia, uma exceção será lançada. As palavras nunca devem ser adicionadas a uma lista de palavras após serem atribuídas a um objeto **RecognizerContext** .

 

Definir um factoid no objeto [**RecognizerContext**](inkrecognizercontext-class.md) também afeta como os dicionários de aplicativo são usados pelo reconhecedor. Os factos que afetam o comportamento dos dicionários são:

-   **Palavras**
-   **SystemDictionary**
-   **Nenhuma**

De longe, o factor mais útil para dicionários de aplicativo é o factor de **listas de palavras** . O facto de lista de **palavras** ajusta o reconhecedor para retornar apenas palavras encontradas na lista de palavras. Esse factor desativa todos os outros dicionários, exceto a lista de palavras. Se o factor de lista de **palavras** estiver definido, e não for especificada nenhuma forma de palavra no contexto do reconhecedor, o dicionário do usuário será usado como a lista de palavras.

Por exemplo, se você estiver criando um aplicativo de partes de avião com um campo que aceite um dos dez nomes de partes especializadas, você poderá criar uma lista de palavras que contenha apenas esses nomes de parte. Definir o facto da área de **palavras** para o campo melhora muito o reconhecimento das palavras inseridas nesse campo. O reconhecedor não precisa escolher entre palavras no dicionário do sistema e palavras na lista de palavras.

O factor **SystemDictionary** só habilita o dicionário do sistema. O factor **None** desabilita todos os dicionários. Esses dois factos são usados para aumentar a precisão do reconhecimento em determinadas instâncias. No entanto, como eles desabilitam os dicionários de aplicativo, eles raramente são usados em conjunto com os dicionários de aplicativo.

Para obter mais informações sobre como os factos afetam o reconhecimento, consulte [usando o contexto para melhorar a precisão](using-context-to-improve-accuracy.md).

Para obter mais informações sobre os factos **SystemDictionary** e **None** , consulte as [edições com suporte na versão 1](supported-factoids-from-version-1.md).

 

 



