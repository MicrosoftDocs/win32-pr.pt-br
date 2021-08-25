---
title: Aplicando uma atualização a um catálogo
description: Aplicando uma atualização a um catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player lojas online, aplicando atualizações aos catálogos
- lojas online, aplicando atualizações aos catálogos
- Digite 1 lojas online, aplicando atualizações aos catálogos
- Windows Media Player lojas online, atualizando catálogos
- lojas online, atualizando catálogos
- Digite 1 lojas online, atualizando catálogos
- Windows Media Player lojas online, atualizações de catálogo
- lojas online, atualizações de catálogo
- Digite 1 lojas online, atualizações de catálogo
- atualizações do catálogo
- Atualizando catálogos
- aplicando atualizações aos catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114b5b341df1101b221a3d8227bf0526bfa32af744f1dca7b0a53ca2d7793c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124026"
---
# <a name="applying-an-update-to-a-catalog"></a>Aplicando uma atualização a um catálogo

> [!Note]  
> Isso normalmente não é feito, exceto para fins de diagnóstico, por exemplo, para ajudar a verificar se um arquivo de diferença é válido. O catálogo gerado dessa maneira não está em formato compactado e não deve ser passado para Windows Media Player.

 

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



 

 

 




