---
title: Propriedade CounterItem.Color
description: Recupera ou define a cor usada para grafar o valor do contador.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propriedade color SysMon
- Propriedade color SysMon, classe CounterItem
- Classe CounterItem SysMon, propriedade Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883863"
---
# <a name="counteritemcolor-property"></a>Propriedade CounterItem.Color

Recupera ou define a cor usada para grafar o valor do contador.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valor da propriedade

Cor usada para grafar o valor do contador.

## <a name="remarks"></a>Comentários

Se você não especificar a cor a ser usada, o SYSMON selecionará cores para os primeiros 16 contadores. Se você especificar mais de 16 contadores, o SYSMON reutilizará as mesmas cores dos primeiros 16 contadores. Para ajudar a distinguir os contadores uns dos [](counteritem-linestyle.md) outros, o SYSMON altera o estilo de linha usado para cada múltiplo de 16 contadores até os primeiros 80 contadores. Por exemplo, os primeiros 16 contadores usam um estilo de linha sólido, os próximos 16 usam um estilo de linha tracejada e assim por diante. Em seguida, o [](counteritem-width.md) SYSMON define a largura da linha como 2 para os contadores de 81 a 96 e para 3 para os contadores 96 a 112. Se a coleção contiver mais de 112 contadores, os contadores conterão valores duplicados de cor, estilo de linha e largura.

**Antes do Windows Vista:** Se você não especificar a cor a ser usada, o SYSMON selecionará cores para os primeiros 16 contadores. Se você especificar mais de 16 contadores, o SYSMON reutilizará as mesmas cores dos primeiros 16 contadores. Para ajudar a distinguir os contadores um do [](counteritem-width.md) outro, o SYSMON aumenta a largura da linha dos três primeiros contadores que recebem a mesma atribuição de cor. Se mais de três contadores usarem a mesma cor, o SYSMON escolherá aleatoriamente a largura da linha a ser usada para o contador.

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

 

 





