---
title: Propriedade MyItem. Width
description: Recupera ou define a largura da linha usada para grafar o valor do contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propriedade Width SysMon
- Propriedade Width SysMon, classe de coitem
- Classe monoitem SysMon, Propriedade Width
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
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644721"
---
# <a name="counteritemwidth-property"></a>Propriedade MyItem. Width

Recupera ou define a largura da linha usada para grafar o valor do contador.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
Property Width As Long
```



## <a name="property-value"></a>Valor da propriedade

Largura da linha usada em um gráfico de linhas. Os valores válidos variam de 1 a 3, em que 1 (o valor padrão) é a largura mais estreita.

**Antes do Windows Vista:** Os valores válidos variam de 1 a 9. Não use um valor de largura maior que 3 se seu aplicativo for executado no Windows Vista.

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                              |
|------------------------------|----------------------------------------|
| **System. ArgumentException** | A largura da linha especificada não é válida. |



 

## <a name="remarks"></a>Comentários

A largura de linha padrão para os primeiros dezesseis contadores que você adiciona é 1. A largura de linha padrão para os próximos dezesseis contadores (contadores 17-32) que você adiciona é 2. A largura de linha padrão para os próximos dezesseis contadores (contadores 33-48) que você adiciona é 3. Depois disso, o SYSMON escolhe aleatoriamente a largura da linha. Para obter detalhes, consulte [**MyItem. Color**](counteritem-color.md).

Para especificar um [**estilo de linha**](counteritem-linestyle.md) diferente de sólido, a largura deve ser 1. Se você especificar um valor maior que 1 e especificar um estilo de linha não sólido, o SYSMON ignorará a largura da linha especificada.

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

 

 





