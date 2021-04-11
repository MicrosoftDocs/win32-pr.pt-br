---
description: Obtém um ícone de dispositivo personalizado.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Método IWiaUIExtension:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090500"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Método IWiaUIExtension:: GetDeviceIcon

Obtém um ícone de dispositivo personalizado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceId* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.

</dd> <dt>

*phIcon* \[ fora\]
</dt> <dd>

Tipo: **HICON \** _

Aponta para um local de memória que receberá um identificador para o ícone do dispositivo.

</dd> <dt>

_nSize * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Especifica o tamanho do ícone desejado, em pixels. O ícone é considerado quadrado e nSize especifica a largura e a altura do ícone solicitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




