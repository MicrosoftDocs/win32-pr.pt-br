---
title: Mensagem de PSM_INDEXTOID (Prsht. h)
description: Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Controles de PSM_INDEXTOID de mensagens do Windows
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
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009521"
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

## <a name="return-value"></a>Retornar valor

Retorna a ID de recurso da página da folha de propriedades especificada por *wParam* , se bem-sucedida. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





