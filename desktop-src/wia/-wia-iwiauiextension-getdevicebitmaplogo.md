---
description: Obtém um logotipo de bitmap personalizado para o dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Método IWiaUIExtension:: GetDeviceBitmapLogo (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763257"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>Método IWiaUIExtension:: GetDeviceBitmapLogo

Obtém um logotipo de bitmap personalizado para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceId* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.

</dd> <dt>

*phBitmap* \[ fora\]
</dt> <dd>

Tipo: **HBITMAP \** _

Aponta para um local de memória que receberá um identificador para o logotipo de bitmap do dispositivo.

</dd> <dt>

_nMaxWidth * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Especifica a largura desejada do bitmap.

</dd> <dt>

*nMaxHeight* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Especifica a altura desejada do bitmap.

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



 

 




