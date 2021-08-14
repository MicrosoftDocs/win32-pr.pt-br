---
description: ICE95 verifica a tabela Control e a tabela BBControl para verificar se os controles do cabrão se ajustam a todos os botões.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315256"
---
# <a name="ice95"></a>ICE95

ICE95 verifica a [tabela Control e](control-table.md) a tabela [BBControl](bbcontrol-table.md) para verificar se os controles do cabrão se ajustam a todos os botões.

## <a name="result"></a>Resultado

Se qualquer uma das seguintes condições for verdadeira, um controle de mío não se ajustará em um cabarão. ICE95 posta os avisos a seguir.



| Aviso ICE95                                                                                                                                                                                                              | Description                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| O item BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não se ajusta a todos os controles de cabisão na tabela Control. A coordenada X excede o limite da largura mínima do controle de minimão %s                   | A coordenada X do controle está fora da largura do quadro.                          |
| O item BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não se ajusta a todos os controles de cabisão na tabela Control. A coordenada Y excede o limite da altura mínima do controle de cúbito %s                  | A coordenada Y do controle está abaixo da parte inferior do painel.                           |
| O item BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não se ajusta a todos os controles de cabisão na tabela Control. A coordenada X e a largura combinadas juntas excedem a largura mínima do controle de mamão %s   | A coordenada X do controle mais a largura do controle está fora da largura da coluna. |
| O item BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não se ajusta a todos os controles de cabisão na tabela Control. A coordenada Y e a altura combinadas excedem a altura mínima do controle de mamão %s | A coordenada Y do controle mais a altura do controle está abaixo da parte inferior do painel. |



 

## <a name="example"></a>Exemplo

O ICE95 relata os seguintes avisos para o exemplo:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Tabela de controle (parcial) (parcial)



| Control  | Tipo      | Largura | Altura |
|----------|-----------|-------|--------|
| control1 | Outdoor | 300   | 100    |
| Control2 | Outdoor | 100   | 300    |



 

[Tabela BBControl](bbcontrol-table.md)



| Outdoor\_ | BBControl  | X   | Y   | Largura | Altura |
|-------------|------------|-----|-----|-------|--------|
| ol1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| ol1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| ol1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| ol1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



