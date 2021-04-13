---
title: Método IMsTscAxEvents OnRemoteWindowDisplayed
description: Chamado quando uma janela do RemoteApp é exibida.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteWindowDisplayed
- Método OnRemoteWindowDisplayed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteWindowDisplayed
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
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369727"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Método IMsTscAxEvents:: OnRemoteWindowDisplayed

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

*vbDisplayed* \[ no\]
</dt> <dd>

Tipo: **\_ booliano de variante**

Indica se a janela do RemoteApp é exibida ou oculta.

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Tipo: **HWND**

O identificador da janela exibida.

</dd> <dt>

*janelaattribute* \[ no\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Um valor da enumeração [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica mais informações sobre o evento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





