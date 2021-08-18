---
title: TTM_GETCURRENTTOOL mensagem (Commctrl.h)
description: Recupera as informações da ferramenta atual em um controle de dica de ferramenta.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL controles de Windows mensagem
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4558e582e4619cd7d96380a1e38e2efe68808b9241e4c627e12a74946965d8de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769336"
---
# <a name="ttm_getcurrenttool-message"></a>Mensagem \_ GETCURRENTTOOL TTM

Recupera as informações da ferramenta atual em um controle de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recebe informações sobre a ferramenta atual. Se esse valor for **NULL,** o valor de retorno indicará a existência da ferramenta atual sem realmente recuperar as informações da ferramenta. Se esse valor não for **NULL,** o **membro cbSize** da estrutura **TOOLINFO** deverá ser preenchido antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário. Se *lParam* for **NULL,** retornará diferente de zero se houver uma ferramenta atual ou zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





