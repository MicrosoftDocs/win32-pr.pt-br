---
description: ICE58 verifica se a tabela de mídia não tem mais de 80 linhas.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528225"
---
# <a name="ice58"></a>ICE58

ICE58 verifica se a [tabela de mídia](media-table.md) não tem mais de 80 linhas.

## <a name="result"></a>Resultado

os avisos relatados pelo ICE58 causam falha na instalação, a menos que o pacote seja instalado com o Windows Installer 2,0 ou posterior. a partir do Windows Installer 2,0, a restrição para mais de 80 entradas de tabela de mídia é removida. Nenhum aviso será emitido se a propriedade de [**Resumo contagem de páginas**](page-count-summary.md) do pacote for maior ou igual a 150. os pacotes de esquema 200 ou superior só podem ser instalados pelo Windows Installer 2,0 ou posterior.

## <a name="example"></a>Exemplo

ICE58 relata os erros e avisos a seguir para o exemplo mostrado.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Para corrigir esse erro, elimine as entradas de tabela de mídia não utilizadas, consolide as entradas de tabela de mídia que se referem à mesma mídia e reempacote seu aplicativo para reduzir a mídia necessária.

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



