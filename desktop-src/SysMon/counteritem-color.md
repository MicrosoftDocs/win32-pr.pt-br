---
title: Propriedade MyItem. Color
description: Recupera ou define a cor usada para grafar o valor do contador.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propriedade Color SysMon
- Propriedade Color SysMon, classe monoitem
- Classe monoitem SysMon, Propriedade Color
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
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644754"
---
# <a name="counteritemcolor-property"></a>Propriedade MyItem. Color

Recupera ou define a cor usada para grafar o valor do contador.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valor da propriedade

A cor usada para grafar o valor do contador.

## <a name="remarks"></a>Comentários

Se você não especificar a cor a ser usada, o SYSMON selecionará as cores dos primeiros dezesseis contadores. Se você especificar mais de dezesseis contadores, o SYSMON reutilizará as mesmas cores dos primeiros dezesseis contadores. Para ajudar a distinguir os contadores um do outro, o SYSMON altera o [**estilo de linha**](counteritem-linestyle.md) usado para cada múltiplo de dezesseis contadores até os primeiros 80 contadores. Por exemplo, os primeiros dezesseis contadores usam um estilo de linha sólida, os próximos dezesseis usam um estilo de linha tracejada e assim por diante. Em seguida, o SYSMON define a [**largura da linha**](counteritem-width.md) como 2 para os contadores 81-96 e 3 para os contadores 96-112. Se a coleção contiver mais de 112 contadores, os contadores conterão valores de cor, de linha e de largura duplicados.

**Antes do Windows Vista:** Se você não especificar a cor a ser usada, o SYSMON selecionará as cores dos primeiros dezesseis contadores. Se você especificar mais de dezesseis contadores, o SYSMON reutilizará as mesmas cores dos primeiros dezesseis contadores. Para ajudar a distinguir os contadores um do outro, o SYSMON aumenta a [**largura da linha**](counteritem-width.md) dos três primeiros contadores que recebem a mesma atribuição de cor. Se mais de três contadores usarem a mesma cor, o SYSMON escolherá aleatoriamente a largura da linha a ser usada para o contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Item**](counteritem.md)
</dt> </dl>

 

 





