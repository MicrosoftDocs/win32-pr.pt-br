---
title: Mensagem de LVM_GETTILEVIEWINFO (commctrl. h)
description: Recupera informações sobre um controle de exibição de lista no modo de exibição de bloco.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- controles de Windows de mensagem de LVM_GETTILEVIEWINFO
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6923f47e4a185ac036a3462a2691036573e8ddfedef9b5f9ab1327ce8204b85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575686"
---
# <a name="lvm_gettileviewinfo-message"></a>\_Mensagem GETTILEVIEWINFO LVM

Recupera informações sobre um controle de exibição de lista no modo de exibição de bloco.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que recebe as informações recuperadas.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





