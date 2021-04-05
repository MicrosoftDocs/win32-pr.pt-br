---
title: Mensagem de TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera os estilos estendidos que estão em uso no momento para o controle de guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Extended TabCtrl.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Controles de TCM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919020"
---
# <a name="tcm_getextendedstyle-message"></a>Mensagem do TCM \_ Extended

Recupera os estilos estendidos que estão em uso no momento para o controle de guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ Extended TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que representa os estilos estendidos em uso no momento para o controle de guia. Esse valor é uma combinação de [estilos estendidos](tab-control-extended-styles.md)de controle de guia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TCM \_ SETextendedattribute**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





