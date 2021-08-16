---
description: Por padrão, o reconhecedor usa um dicionário do sistema que contém todas as palavras normalmente escritas em uma linguagem.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Usando dicionários de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c83013f704fe28b5754ab89fd95ed730e16d1cda5ab257d4fb411d0e7293347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449228"
---
# <a name="using-application-dictionaries"></a>Usando dicionários de aplicativos

Por padrão, o reconhecedor usa um dicionário do sistema que contém todas as palavras normalmente escritas em uma linguagem. Além disso, o reconhecedor tem um dicionário do usuário que contém palavras que o usuário adicionou ao dicionário. Os usuários adicionam uma palavra ao dicionário do usuário por meio do painel de entrada do Tablet PC por meio de seleções em:

-   A lista alternativa (ao escrever).
-   O menu ferramentas de fala (quando estiver falando).

Se você estiver criando um aplicativo no qual você prevê que o usuário irá gravar palavras que não são encontradas no dicionário do sistema ou no dicionário do usuário, crie um dicionário de aplicativos. Um dicionário de aplicativos melhora ainda mais a precisão do reconhecimento ao fornecer ao reconhecedor uma lista personalizada adicional de palavras que provavelmente serão inseridas como manuscritos em um aplicativo.

Você cria um dicionário de aplicativos usando o objeto de [**listas de palavras**](inkwordlist-class.md) . O dicionário de aplicativos incorretos aumenta a precisão do reconhecimento fornecendo ao reconhecedor uma lista de palavras esperadas. Por exemplo, um dicionário de aplicativo que contém a terminologia médica aumenta a precisão do reconhecimento dentro de um aplicativo desenvolvido para o setor médico no qual os termos provavelmente serão escritos.

Como outro exemplo, ao criar um formulário para alguém solicitar instrumentos musicais, crie um objeto de [**listas de palavras**](inkwordlist-class.md) que contenha os nomes dos fabricantes de instrumentos mais comuns. Defina a propriedade de [**listas de palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) para o objeto de faixa de **palavras** que você criou. Em seguida, essa lista de palavras é passada para o reconhecedor pelo objeto **RecognizerContext** . O dicionário do aplicativo aumenta a precisão do reconhecimento quando esses nomes são gravados em um campo no aplicativo.

Os tópicos a seguir descrevem como usar dicionários de aplicativo.

-   [Compreendendo as listas de palavras, o contexto do reconhecedor e as chaves](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Criando dicionários personalizados para reconhecimento de manuscrito](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



