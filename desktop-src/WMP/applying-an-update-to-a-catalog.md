---
title: Aplicando uma atualização a um catálogo
description: Aplicando uma atualização a um catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Lojas online do Windows Media Player, aplicando atualizações aos catálogos
- lojas online, aplicando atualizações aos catálogos
- Digite 1 lojas online, aplicando atualizações aos catálogos
- Armazenamentos online do Windows Media Player, atualizando catálogos
- lojas online, atualizando catálogos
- Digite 1 lojas online, atualizando catálogos
- Armazenamentos online do Windows Media Player, atualizações de catálogo
- lojas online, atualizações de catálogo
- Digite 1 lojas online, atualizações de catálogo
- atualizações do catálogo
- Atualizando catálogos
- aplicando atualizações aos catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761490"
---
# <a name="applying-an-update-to-a-catalog"></a>Aplicando uma atualização a um catálogo

> [!Note]  
> Isso normalmente não é feito, exceto para fins de diagnóstico, por exemplo, para ajudar a verificar se um arquivo de diferença é válido. O catálogo gerado dessa maneira não está em formato compactado e não deve ser passado para o Windows Media Player.

 

Um novo arquivo de catálogo pode ser criado usando a sintaxe abaixo, em que *inputcatalog* é o local do catálogo original e *inputdiff* é o local do arquivo de diferenças a ser aplicado. Os arquivos de catálogo devem estar em formato descompactado.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Por exemplo, o seguinte cria um novo catálogo de C: \\ Catalog210 \\ Catalog. wmdb e C: \\ Catalog210 \\ Catalog. diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Se a compilação for bem-sucedida, catcomp.exe criará os arquivos de saída a seguir.



| Nome do arquivo        | Descrição       |
|------------------|-------------------|
| Catalog. wmdb. New | Novo arquivo de catálogo. |



 

 

 




