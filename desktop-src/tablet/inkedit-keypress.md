---
description: Ocorre quando o usuário pressiona e libera uma tecla enquanto o controle InkEdit tem foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713100edeae3ce6b950433afb73d13f40aefb291047e98984cbd6908dde3ce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935092"
---
# <a name="inkeditkeypress-event"></a>Evento InkEdit. KeyPress

Ocorre quando o usuário pressiona e libera uma tecla enquanto o controle [InkEdit](inkedit-control-reference.md) tem foco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Char* 
</dt> <dd>

Um inteiro que retorna um código de keyansi numérico padrão. O parâmetro *Char* é passado por referência; alterá-lo envia um caractere diferente para o controle. Alterar o parâmetro *Char* para 0 cancela o evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeKeyPress DISPID.

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
</dt> <dt>

[**Controle de evento InkEdit de KeyDown \[\]**](inkedit-keydown.md)
</dt> <dt>

[**Controle de evento InkEdit de KeyUp \[\]**](inkedit-keyup.md)
</dt> </dl>

 

