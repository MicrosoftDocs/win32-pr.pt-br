---
description: Ocorre quando o controle InkEdit é clicado duas vezes.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Evento InkEdit. DblClick (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2f1cf2a7b7d7d699af5cd8a148e5c54a2879ad5eb879bd34af7531025748e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032084"
---
# <a name="inkeditdblclick-event"></a>Evento InkEdit. DblClick

Ocorre quando o controle [InkEdit](inkedit-control-reference.md) é clicado duas vezes.

## <a name="syntax"></a>Sintaxe


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) . Se houver código no evento de [**clique**](inkedit-click.md) , o evento **DblClick** nunca será disparado.

 

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeDblClick DISPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




