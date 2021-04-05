---
title: Mensagem de LB_GETITEMHEIGHT (WinUser. h)
description: Obtém a altura dos itens em uma caixa de listagem.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Controles de LB_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824338"
---
# <a name="lb_getitemheight-message"></a>GETITEMHEIGHT de mensagens de LB \_

Obtém a altura dos itens em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item da caixa de listagem. Esse índice será usado somente se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ; caso contrário, ela deverá ser zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é a altura, em pixels, de cada item na caixa de listagem. O valor de retorno é a altura do item especificado pelo parâmetro *wParam* se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) . O valor de retorno será um erro de LB \_ se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETITEMHEIGHT lb**](lb-setitemheight.md)
</dt> </dl>

 

 





