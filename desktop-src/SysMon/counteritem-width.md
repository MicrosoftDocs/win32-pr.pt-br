---
title: Propriedade CounterItem.Width
description: Recupera ou define a largura da linha usada para grafar o valor do contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propriedade Width SysMon
- Propriedade width SysMon, classe CounterItem
- Classe CounterItem SysMon, propriedade Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5deca3d7fa188c834f2ca952c9b6c4760a3a1b56c83eb8250e343257b8108de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883502"
---
# <a name="counteritemwidth-property"></a>Propriedade CounterItem.Width

Recupera ou define a largura da linha usada para grafar o valor do contador.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property Width As Long
```



## <a name="property-value"></a>Valor da propriedade

Largura de linha usada em um grafo de linha. Os valores válidos variam de 1 a 3, em que 1 (o valor padrão) é a largura mais estreita.

**Antes do Windows Vista:** Os valores válidos variam de 1 a 9. Não use um valor de largura maior que 3 se o aplicativo for executado no Windows Vista.

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | A largura de linha especificada não é válida. |



 

## <a name="remarks"></a>Comentários

A largura de linha padrão para os primeiros 16 contadores que você adiciona é 1. A largura de linha padrão para os próximos 16 contadores (contadores de 17 a 32) que você adiciona é 2. A largura de linha padrão para os próximos 16 contadores (contadores de 33 a 48) que você adiciona é 3. Depois disso, o SYSMON escolhe aleatoriamente a largura da linha. Para obter detalhes, consulte [**CounterItem.Color**](counteritem-color.md).

Para especificar um [**estilo de linha**](counteritem-linestyle.md) diferente de sólido, a largura deve ser 1. Se você especificar um valor maior que 1 e especificar um estilo de linha não sólido, o SYSMON ignorará a largura de linha especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





