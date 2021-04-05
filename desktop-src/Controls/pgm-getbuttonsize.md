---
title: Mensagem de PGM_GETBUTTONSIZE (commctrl. h)
description: Recupera o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro getbuttons do pager.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Controles de PGM_GETBUTTONSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009557"
---
# <a name="pgm_getbuttonsize-message"></a>\_Mensagem de GETbuttons do PGM

Recupera o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que contém o tamanho do botão atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetButtons do PGM \_**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





