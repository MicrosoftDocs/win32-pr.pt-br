---
title: Estrutura XML do arquivo de definição de aparência
description: Estrutura XML do arquivo de definição de aparência
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- Criando capas, arquivos de definição de capa
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, estrutura XML
- Estrutura XML para arquivos de definição de capa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005784"
---
# <a name="skin-definition-file-xml-structure"></a>Estrutura XML do arquivo de definição de aparência

O arquivo de definição de capa é escrito em XML. Um dos recursos importantes do XML é que ele é totalmente estruturado e é semelhante a uma estrutura de tópicos. O código XML é simplesmente uma série de elementos, como **View** e **Button**. Você começará com os elementos e, em seguida, os definirá com atributos. O restante deste tutorial fornecerá detalhes sobre os atributos, mas aqui está o contorno dos elementos que serão usados:


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



Tendo em mente a estrutura simples dos elementos, você pode fazer sentido dos atributos que tornam cada elemento exclusivo. Os detalhes de cada elemento serão abordados nos tópicos restantes desta seção. Para obter mais informações sobre elementos e atributos, consulte a [referência de programação de capa](skin-programming-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




