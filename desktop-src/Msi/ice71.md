---
description: ICE71 verifica se a tabela de mídia contém uma entrada com DiskId igual a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142510"
---
# <a name="ice71"></a>ICE71

ICE71 verifica se a [tabela de mídia](media-table.md) contém uma entrada com DiskId igual a 1. (Windows Installer pressupõe que o pacote de .msi está no disco 1.)

## <a name="result"></a>Resultado

ICE71 retornará um erro se a tabela de mídia não contiver uma entrada com DiskId igual a 1.

## <a name="example"></a>Exemplo

ICE71 relata o seguinte erro para o exemplo mostrado.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 corrigir esse erro, altere a DiskId da entrada onde o pacote está armazenado em 1.

[Tabela de mídia](media-table.md) (parcial)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



