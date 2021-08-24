---
title: Chamando Funções
description: Chamando Funções
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player capas, chamando funções em JScript
- skins, chamando funções em JScript
- chamando funções no JScript
- JScript arquivos para capas, funções de chamada
- Windows Media Player capas, atributo scriptFile no JScript
- skins,atributo scriptFile no JScript
- attributes,scriptFile no JScript
- Atributo scriptFile no JScript
- JScript arquivos para capas, atributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764266"
---
# <a name="calling-functions"></a>Chamando Funções

Se você precisar chamar mais de algumas linhas de código, poderá carregar um arquivo de script usando o **atributo scriptFile** do elemento **VIEW** e chamar as funções no script. Você pode carregar mais de um arquivo por exibição:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Depois que os arquivos de script são carregados, você pode chamar funções neles de dentro da seção Exibição. Por exemplo, para chamar uma função chamada *myfunction* quando algo é clicado, digite o seguinte:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Se você tiver mais de uma exibição, somente as funções nos arquivos carregados na exibição atual estarão disponíveis para o código XML e JScript em execução com a exibição atual. Os arquivos carregados em outras exibições não estão no escopo com a exibição atual.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando JScript**](using-jscript.md)
</dt> </dl>

 

 




