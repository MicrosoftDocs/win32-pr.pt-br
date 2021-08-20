---
description: Indique que o final do fluxo de mídia foi atingido.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: Método IMFMediaSourceExtension::SetEndOfStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 29937a939dd8d087e1a70224950ddd8d14eea8989127dc9f33c2747468db4b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062965"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>Método IMFMediaSourceExtension::SetEndOfStream

Indique que o final do fluxo de mídia foi atingido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*erro* \[ Em\]
</dt> <dd>

Usado para passar informações de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[**ERRO \_ MF MSE \_**](mf-mse-error.md)
</dt> </dl>

 

 




