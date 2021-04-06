---
title: Mensagem de CCM_GETVERSION (commctrl. h)
description: Obtém o número de versão de um conjunto de controle pela mensagem CCM \_ SetVersion mais recente.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Controles de CCM_GETVERSION de mensagens do Windows
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
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085833"
---
# <a name="ccm_getversion-message"></a>\_Mensagem CCM GETversion

Obtém o número de versão de um conjunto de controle pela mensagem [**CCM \_ SetVersion**](ccm-setversion.md) mais recente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de versão definido pela mensagem CCM mais recente da [**\_ objectVersion**](ccm-setversion.md) . Se nenhuma mensagem desse tipo tiver sido enviada, ela retornará zero.

## <a name="remarks"></a>Comentários

Essa mensagem não retorna a versão da DLL. Confira [versões do Shell](common-control-versions.md) para obter uma discussão de como usar o [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar a versão atual da dll.

> [!Note]  
> O número de versão é definido com base em controle por controle e pode não ser o mesmo para todos os controles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

