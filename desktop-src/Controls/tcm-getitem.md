---
title: Mensagem de TCM_GETITEM (commctrl. h)
description: Recupera informações sobre uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Controles de TCM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749669"
---
# <a name="tcm_getitem-message"></a>\_Mensagem GETITEM de TCM

Recupera informações sobre uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da guia.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica as informações para recuperar e receber informações sobre a guia. Quando a mensagem é enviada, o membro de **máscara** especifica quais atributos retornar. Se o membro de **máscara** especificar o \_ valor de texto TCIF, o membro **pszText** deverá conter o endereço do buffer que receberá o texto do item e o membro **cchTextMax** deverá especificar o tamanho do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o \_ sinalizador de texto TCIF for definido no membro **Mask** da estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado. O controle pode definir o membro **pszText** como **nulo** para indicar que nenhum texto está associado ao item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) e **TCM \_ getitema** (ANSI)<br/>                   |



 

 





