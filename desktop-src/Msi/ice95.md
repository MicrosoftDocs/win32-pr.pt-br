---
description: ICE95 verifica a tabela de controle e a tabela BBControl para verificar se os controles de mural se encaixam em todas as suas murals.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171137"
---
# <a name="ice95"></a>ICE95

ICE95 verifica a [tabela de controle](control-table.md) e a [tabela BBControl](bbcontrol-table.md) para verificar se os controles de mural se encaixam em todas as suas murals.

## <a name="result"></a>Resultado

Se qualquer uma das seguintes opções for verdadeira, um controle de mensagem não caberá em um mural. ICE95 posta os seguintes avisos.



| Aviso de ICE95                                                                                                                                                                                                              | Descrição                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle. A coordenada X excede o limite da largura mínima do controle do mural% s                   | A coordenada X do controle está fora da largura do mural.                          |
| O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle. A coordenada Y excede o limite da altura mínima do controle do mural% s                  | A coordenada Y do controle está abaixo da parte inferior do mural.                           |
| O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle. A coordenada X e a largura combinadas em conjunto excedem a largura mínima do controle do mural% s   | A coordenada X do controle mais a largura do controle está fora da largura do mural. |
| O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle. A coordenada Y e a altura combinadas em conjunto excedem a altura mínima de controle do mural% s | A coordenada Y do controle mais a altura do controle está abaixo da parte inferior do mural. |



 

## <a name="example"></a>Exemplo

ICE95 relata os seguintes avisos para o exemplo:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Tabela de controle (parcial) (parcial)



| Control  | Tipo      | Largura | Altura |
|----------|-----------|-------|--------|
| Control1 | Mensagem | 300   | 100    |
| Control2 | Mensagem | 100   | 300    |



 

[Tabela BBControl](bbcontrol-table.md)



| Mensagem\_ | BBControl  | X   | S   | Largura | Altura |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



