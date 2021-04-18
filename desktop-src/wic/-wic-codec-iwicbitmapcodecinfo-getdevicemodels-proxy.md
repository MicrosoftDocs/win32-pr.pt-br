---
description: Função de proxy para o método GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: Função IWICBitmapCodecInfo_GetDeviceModels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812296"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>\_Função de \_ proxy IWICBitmapCodecInfo GetDeviceModels

Função de proxy para o método [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Ponteiro para este objeto [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchDeviceModels* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho do buffer de modelos de dispositivo.

</dd> <dt>

*wzDeviceModels* \[ entrada, saída\]
</dt> <dd>

Tipo: **WCHAR \** _

Um ponteiro que recebe uma lista delimitada por vírgulas de nomes de modelo de dispositivo associados ao codec.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Tipo: **uint \** _

O tamanho de buffer real necessário para recuperar todos os nomes de modelo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




