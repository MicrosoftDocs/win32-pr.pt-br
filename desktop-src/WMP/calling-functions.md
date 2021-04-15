---
title: Chamando Funções
description: Chamando Funções
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Capas do Windows Media Player, chamando funções no JScript
- capas, chamando funções no JScript
- chamando funções no JScript
- Arquivos JScript para capas, chamando funções
- Capas do Windows Media Player, atributo scriptfile no JScript
- Skins, atributo scriptfile no JScript
- atributos, scriptfile em JScript
- atributo scriptfile no JScript
- Arquivos JScript para capas, atributo scriptfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498807"
---
# <a name="calling-functions"></a>Chamando Funções

Se você precisar chamar mais de algumas linhas de código, poderá carregar um arquivo de script usando o atributo **scriptfile** do elemento **View** e chamar as funções no script. Você pode carregar mais de um arquivo por exibição:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Depois que os arquivos de script são carregados, você pode chamar funções neles de dentro de sua seção de exibição. Por exemplo, para chamar uma função chamada *MyFunction* quando algo é clicado, digite o seguinte:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Se você tiver mais de uma exibição, somente as funções em arquivos carregados no modo de exibição atual estarão disponíveis para o código XML e JScript em execução com a exibição atual. Os arquivos carregados em outras exibições não estão no escopo com a exibição atual.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o JScript**](using-jscript.md)
</dt> </dl>

 

 




