---
title: Mensagem de PSM_INDEXTOID (Prsht. h)
description: Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- controles de Windows de mensagem de PSM_INDEXTOID
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7a26cd97d324ae9bb4cfee85df00387c59293c7de8817b67da5605a207f07f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985716"
---
# <a name="psm_indextoid-message"></a>Mensagem de PSM \_ INDEXTOID

Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da página.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a ID de recurso da página da folha de propriedades especificada por *wParam* , se bem-sucedida. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





