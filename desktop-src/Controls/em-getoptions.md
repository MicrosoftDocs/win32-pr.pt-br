---
title: Mensagem de EM_GETOPTIONS (RichEdit. h)
description: Recupera opções de controle de edição avançadas.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- Controles de EM_GETOPTIONS de mensagens do Windows
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
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918802"
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

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna uma combinação dos valores de sinalizador de opção atual descritos na mensagem em [**\_ setoptionss**](em-setoptions.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SEToptions**](em-setoptions.md)
</dt> </dl>

 

 





