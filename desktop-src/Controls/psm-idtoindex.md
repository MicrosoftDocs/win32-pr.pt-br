---
title: Mensagem de PSM_IDTOINDEX (Prsht. h)
description: Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Controles de PSM_IDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086087"
---
# <a name="psm_idtoindex-message"></a>Mensagem de PSM \_ IDTOINDEX

Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

ID de recurso da página.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice de base zero da página da folha de propriedades especificada por *lParam* , se obtiver êxito. Caso contrário, ele retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





