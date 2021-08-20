---
title: Mensagem de HDM_HITTEST (commctrl. h)
description: Testa um ponto para determinar qual item de cabeçalho, se houver, está no ponto especificado.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- controles de Windows de mensagem de HDM_HITTEST
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
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544766"
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

## <a name="return-value"></a>Valor retornado

Retorna o índice do item na posição especificada, se houver, ou 1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





