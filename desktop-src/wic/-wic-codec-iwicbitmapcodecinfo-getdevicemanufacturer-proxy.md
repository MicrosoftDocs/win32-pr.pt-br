---
description: Função de proxy para o método GetDeviceManufacturer.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: Função IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788659"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a>\_Função de \_ proxy IWICBitmapCodecInfo GetDeviceManufacturer

Função de proxy para o método [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
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

*cchDeviceManufacturer* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho do nome do fabricante do dispositivo.

</dd> <dt>

*wzDeviceManufacturer* \[ entrada, saída\]
</dt> <dd>

Tipo: **WCHAR \** _

Um ponteiro que recebe o nome do fabricante do dispositivo.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Tipo: **uint \** _

O tamanho real do buffer necessário para recuperar o nome do fabricante do dispositivo.

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



 

 




