---
title: TCM_SETITEM mensagem (Commctrl.h)
description: Define alguns ou todos os atributos de uma guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM controles de Windows mensagem
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27f93e2743e5676c0fcca932cfa1936bb72667ef4fa4a5334eaae3e78d2be08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876317"
---
# <a name="tcm_setitem-message"></a>Mensagem TCM \_ SETITEM

Define alguns ou todos os atributos de uma guia. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contém os novos atributos de item. O **membro mask** especifica quais atributos definir. Se o **membro mask** especificar o valor de TCIF TEXT, o membro pszText será o endereço de uma cadeia de caracteres terminada em nulo e o membro \_ **cchTextMax** será ignorado. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) e **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





