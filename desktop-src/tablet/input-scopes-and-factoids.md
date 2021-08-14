---
description: Descreve como os escopos de entrada são usados para reconhecimento.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Escopos de entrada e factores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881ebd26cbfb70cb215103b9a6face356af078e47b74a2e9140886f81f457eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450966"
---
# <a name="input-scopes-and-factoids"></a>Escopos de entrada e factores

Um escopo de entrada é um conjunto definido de palavras, números, pontuação e ordenações sintáticas que são permitidas em um determinado modelo de linguagem. Os escopos de entrada podem ser usados por aplicativos para restringir o modelo de linguagem usado pelo reconhecedor a um contexto específico. Por exemplo, um escopo de entrada é \_ SMTPEMAILADDRESS de email \_ influencia os resultados de reconhecimento indicando que um campo específico é um endereço de email. Assim, é provável que o campo contenha caracteres como " @" and " \_ ", e não pode conter caracteres como " \* " e espaços.

> [!Note]  
> Outras tecnologias da Microsoft também usam escopos de entrada. Este artigo se concentra no uso de contexto para melhorar a precisão dos mecanismos de reconhecimento de manuscrito para aplicativos do Tablet PC.

 

As versões anteriores da API de tecnologia do Tablet PC usaram os factos para definir o contexto. Para fins práticos, um factor é a mesma coisa que um escopo de entrada. A versão um da plataforma do SDK do Tablet PC definiu um conjunto de valores de facto no objeto de [**factor**](factoid-constants.md) . Esses valores foram usados para definir o contexto e influenciar os resultados do reconhecimento ao usar o objeto [**RecognizerContext**](inkrecognizercontext-class.md) para reconhecimento. para os reconhecedores do script latino a partir do Windows XP Tablet PC Edition 2005, você ainda usa a propriedade [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do objeto **RecognizerContext** para definir o contexto, mas você deve passar um escopo de entrada, uma lista de frases ou um valor de expressão regular de manuscrito em vez de um dos valores da versão um factor. Os reconhecedores da Microsoft dos caracteres do leste asiático não dão suporte ao uso dos valores enumerados do escopo de entrada. Você deve continuar usando valores de factor para reconhecedores de caracteres do leste asiático.

Os escopos de entrada e as chaves são restrições nas alternativas de nível de palavra; as alternativas de caracteres podem estar fora do escopo de entrada especificado mesmo quando o sinalizador de **coerção** está definido.

Quando o sinalizador de **coerção** é definido com um factor restritivo, pode acontecer que o reconhecedor não possa produzir uma resposta que corresponda à tinta e satisfaça o factor. Outro cenário em que o reconhecedor pode não produzir nenhuma resposta satisfatória é quando o idioma do reconhecedor não corresponde ao idioma da tinta (por exemplo, o reconhecedor em inglês americano e os caracteres de tinta do chinês).

Quando o reconhecedor de manuscrito não consegue reconhecer a tinta de uma determinada palavra ou caractere, ele pode retornar uma lista alternativa vazia ou uma lista alternativa em que a primeira opção é o ponto de código 0xFFFF (caractere indefinido). Isso é especialmente útil em modos de entrada de guia em caixa, em que cada caixa com tinta deve ter uma lista não vazia de alternativas. O aplicativo pode exibir esse caractere indefinido de qualquer forma que escolher (por exemplo, como "???").

> [!Note]  
> Os valores de factor continuam trabalhando com reconhecedores de script latino para compatibilidade com versões anteriores.

 

Para obter mais informações sobre o factos, consulte [definindo o contexto para controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Para obter informações sobre os refactos do leste asiático, consulte as [edições com suporte na versão 1](supported-factoids-from-version-1.md).

 

 



