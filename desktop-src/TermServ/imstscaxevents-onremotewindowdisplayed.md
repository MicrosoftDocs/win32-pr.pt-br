---
title: Método IMsTscAxEvents OnRemoteWindowDisplayed
description: Chamado quando uma janela do RemoteApp é exibida.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Método OnRemoteWindowDisplayed Serviços de Área de Trabalho Remota
- O método OnRemoteWindowDisplayed Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota método , OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6985a71fe6351a81b2daef69401dfd5c65543e9984fd64c28a120704a34d5a8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512106"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Método IMsTscAxEvents::OnRemoteWindowDisplayed

Chamado quando uma janela do RemoteApp é exibida.

## <a name="syntax"></a>Sintaxe


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vbDisplayed* \[ Em\]
</dt> <dd>

Tipo: **VARIANT \_ BOOL**

Indica se a janela RemoteApp é exibida ou oculta.

</dd> <dt>

*hwnd* \[ Em\]
</dt> <dd>

Digite: **HWND**

O alça da janela exibida.

</dd> <dt>

*windowAttribute* \[ Em\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Um valor da [**enumeração RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica mais informações sobre o evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





