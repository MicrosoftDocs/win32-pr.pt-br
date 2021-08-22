---
title: Mensagem de LVM_HASGROUP (commctrl. h)
description: Determina se o controle de exibição de lista tem um grupo especificado.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- controles de Windows de mensagem de LVM_HASGROUP
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9dcfadf3e7a07a5f814f5421ed97d26faff6a5ac4c36ce97b9faea77c6a152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293736"
---
# <a name="lvm_hasgroup-message"></a>\_Mensagem HASGROUP LVM

Determina se o controle de exibição de lista tem um grupo especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>ID do grupo.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser **NULL**.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se o controle de exibição de lista tiver o grupo especificado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





