---
title: TCM_GETITEM mensagem (Commctrl.h)
description: Recupera informações sobre uma guia em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItem TabCtrl.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM controles Windows mensagem
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
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876576"
---
# <a name="tcm_getitem-message"></a>Mensagem GETITEM do TCM \_

Recupera informações sobre uma guia em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ GetItem TabCtrl.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da guia.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica as informações a recuperar e recebe informações sobre a guia. Quando a mensagem é enviada, o **membro de máscara** especifica quais atributos retornar. Se  o membro mask especificar o valor de TCIF TEXT, o membro pszText deverá conter o endereço do buffer que recebe o texto do item e o membro \_ **cchTextMax** deverá especificar o tamanho do buffer. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Se o sinalizador TEXT TCIF for definido no membro de máscara da estrutura \_ [**TCITEM,**](/windows/win32/api/commctrl/ns-commctrl-tcitema) o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado.  O controle pode definir o **membro pszText** como **NULL** para indicar que nenhum texto está associado ao item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) e **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





