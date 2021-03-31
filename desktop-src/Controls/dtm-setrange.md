---
title: Mensagem de DTM_SETRANGE (commctrl. h)
description: Define os tempos mínimos e máximos de sistema permitidos para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetRange de DateTime.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Controles de DTM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644914"
---
# <a name="dtm_setrange-message"></a>\_Mensagem SETRANGE DTM

Define os tempos mínimos e máximos de sistema permitidos para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetRange de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor que especifica quais valores de intervalo são válidos. Esse parâmetro pode ser uma combinação dos seguintes valores:



| Valor                                                                                                                                          | Significado                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ mín.**</dt> </dl> | O primeiro elemento na matriz de estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) é válido e será usado para definir a hora mínima permitida do sistema.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | O segundo elemento na matriz de estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) é válido e será usado para definir a hora máxima permitida do sistema.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . O primeiro elemento da matriz **SYSTEMTIME** contém o tempo mínimo permitido. O segundo elemento da matriz **SYSTEMTIME** contém o tempo máximo permitido. Não é necessário preencher um elemento de matriz que não esteja especificado no parâmetro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

O seletor de data e hora exibe apenas datas/horários que se enquadram no intervalo especificado, impedindo que o usuário selecione uma data e hora que esteja fora do intervalo. Se a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) especificar uma data e hora que esteja fora do intervalo, ela falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

