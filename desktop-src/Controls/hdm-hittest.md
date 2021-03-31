---
title: Mensagem de HDM_HITTEST (commctrl. h)
description: Testa um ponto para determinar qual item de cabeçalho, se houver, está no ponto especificado.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Controles de HDM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085823"
---
# <a name="hdm_hittest-message"></a>\_Mensagem HDM HITTEST

Testa um ponto para determinar qual item de cabeçalho, se houver, está no ponto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) que contém a posição para testar e receber informações sobre os resultados do teste.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item na posição especificada, se houver, ou 1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





