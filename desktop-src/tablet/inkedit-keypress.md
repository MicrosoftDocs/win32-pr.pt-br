---
description: Ocorre quando o usuário pressiona e libera uma tecla enquanto o controle InkEdit tem foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812039"
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

## <a name="return-value"></a>Retornar valor

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeKeyPress DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Controle de evento InkEdit de KeyDown \[\]**](inkedit-keydown.md)
</dt> <dt>

[**Controle de evento InkEdit de KeyUp \[\]**](inkedit-keyup.md)
</dt> </dl>

 

