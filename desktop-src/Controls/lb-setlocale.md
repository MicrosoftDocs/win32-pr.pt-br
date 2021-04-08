---
title: Mensagem de LB_SETLOCALE (WinUser. h)
description: Define a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o \_ estilo de classificação lbs) e o texto adicionado pela mensagem do lb \_ AddString.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Controles de LB_SETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009652"
---
# <a name="lb_setlocale-message"></a>\_Mensagem SETlocal do lb

Define a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo de [**\_ classificação lbs**](list-box-styles.md) ) e o texto adicionado pela mensagem do [**lb \_ AddString**](lb-addstring.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador de localidade que a caixa de listagem usará para classificar ao adicionar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o identificador de localidade anterior. Se o parâmetro *wParam* especificar uma localidade que não esteja instalada no sistema, o valor de retorno será lb \_ Err e a localidade da caixa de listagem atual não será alterada.

## <a name="remarks"></a>Comentários

Use a macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir um identificador de localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**\_local lb**](lb-getlocale.md)
</dt> </dl>

 

