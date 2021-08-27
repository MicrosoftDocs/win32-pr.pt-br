---
title: Mensagem de PSM_IDTOINDEX (Prsht. h)
description: Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- controles de Windows de mensagem de PSM_IDTOINDEX
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
ms.openlocfilehash: 83bce0bfeecd2f233b2108133b08e49c27c90625c1bd07f2d4273bd77bbd0b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061516"
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

## <a name="return-value"></a>Valor retornado

Retorna o índice de base zero da página da folha de propriedades especificada por *lParam* , se obtiver êxito. Caso contrário, ele retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





