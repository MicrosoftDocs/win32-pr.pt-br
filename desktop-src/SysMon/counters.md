---
title: Coleção de contadores (Isysmon. h)
description: Use essa classe para gerenciar a coleção de objetos de comitem. Para recuperar esse objeto, chame SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Coleção de contadores SysMon
- Coleção de contadores SysMon, descrita
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8349c1425450491c3fc658f6ac1ac3c5fcf75d3e617a92f6e34b91f2f5802e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883333"
---
# <a name="counters-collection"></a>Coleção de contadores

Use essa classe para gerenciar a coleção de objetos de [**comitem**](counteritem.md) .

Para recuperar esse objeto, chame [**SystemMonitor. Counters**](systemmonitor-counters.md).

## <a name="members"></a>Membros

A coleção de **contadores** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A coleção de **contadores** tem esses métodos.



| Método                            | Descrição                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Agrega**](counters-add.md)       | Adiciona uma instância de [**monoitem**](counteritem.md) à coleção.<br/>      |
| [**Remover**](counters-remove.md) | Remove uma instância de [**monoitem**](counteritem.md) da coleção.<br/> |



 

### <a name="properties"></a>Propriedades

A coleção de **contadores** tem essas propriedades.



| Propriedade                                   | Descrição                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contagem**](counters-count.md)<br/> | Recupera o número de instâncias de [**monoitem**](counteritem.md) na coleção.<br/>  |
| [**Item**](counters-item.md)<br/>   | Recupera a instância de [**monoitem**](counteritem.md) especificada da coleção.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **Counters** é a propriedade padrão do objeto [**SystemMonitor**](systemmonitor.md) .

Adicione a essa coleção os contadores que você deseja grafar. O SYSMON recupera os valores do contador do sistema ou de um arquivo de log, dependendo da [**fonte de dados**](systemmonitor-datasourcetype.md) que você especificar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





