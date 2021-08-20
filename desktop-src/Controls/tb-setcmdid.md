---
title: Mensagem de TB_SETCMDID (commctrl. h)
description: Define o identificador de comando de um botão da barra de ferramentas.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- controles de Windows de mensagem de TB_SETCMDID
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539fb03899a6a763a94a7cd2fd1b7e8be071f04e26e21f19e9ff53640b87be1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167601"
---
# <a name="tb_setcmdid-message"></a>TB de \_ mensagem SETCMDID

Define o identificador de comando de um botão da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero do botão cujo identificador de comando deve ser definido.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador do comando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





