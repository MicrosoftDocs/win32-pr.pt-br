---
title: Mensagem de EM_GETOPTIONS (RichEdit. h)
description: Recupera opções de controle de edição avançadas.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- controles de Windows de mensagem de EM_GETOPTIONS
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba85b5fe3ffd47763d25b9ca13bf10f6202a6876e25d300f66d9af3852edd5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019514"
---
# <a name="em_getoptions-message"></a>\_Mensagem em GEToptionss

Recupera opções de controle de edição avançadas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna uma combinação dos valores de sinalizador de opção atual descritos na mensagem em [**\_ setoptionss**](em-setoptions.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SEToptions**](em-setoptions.md)
</dt> </dl>

 

 





