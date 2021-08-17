---
title: Mensagem de IPM_GETADDRESS (commctrl. h)
description: Obtém os valores de endereço para todos os quatro campos no controle de endereço IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- controles de Windows de mensagem de IPM_GETADDRESS
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434506"
---
# <a name="ipm_getaddress-message"></a>\_Mensagem de GETADDRESS IPM

Obtém os valores de endereço para todos os quatro campos no controle de endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um valor **DWORD** que recebe o endereço. O valor do campo 3 estará contido em bits 0 a 7. O valor do campo 2 estará contido em bits 8 a 15. O valor do campo 1 estará contido nos bits 16 a 23. O valor do campo 0 estará contido em bits 24 a 31. O [**primeiro \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**o \_ segundo**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)IPAddress, o [**terceiro \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)e o [**quarto \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros também podem ser usados para extrair as informações de endereço. Zero será retornado como o endereço de qualquer campo em branco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de campos não vazios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





