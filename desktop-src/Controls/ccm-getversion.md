---
title: CCM_GETVERSION mensagem (Commctrl.h)
description: Obtém o número de versão de um conjunto de controles pela mensagem SETVERSION do CCM \_ mais recente.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION controles Windows mensagem
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320256"
---
# <a name="ccm_getversion-message"></a>Mensagem \_ GETVERSION do CCM

Obtém o número de versão de um conjunto de controles pela mensagem [**\_ SETVERSION**](ccm-setversion.md) do CCM mais recente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de versão definido pela mensagem [**\_ SETVERSION do CCM mais**](ccm-setversion.md) recente. Se nenhuma mensagem desse tipo tiver sido enviada, ela retornará zero.

## <a name="remarks"></a>Comentários

Essa mensagem não retorna a versão da DLL. Confira [Versões do Shell](common-control-versions.md) para obter uma discussão sobre como usar [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar a versão atual da DLL.

> [!Note]  
> O número de versão é definido por controle e pode não ser o mesmo para todos os controles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

