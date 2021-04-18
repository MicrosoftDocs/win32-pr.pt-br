---
description: Função de proxy para o método CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: Função IWICImagingFactory_CreateEncoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814110"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a>\_Função de proxy Createencoderr IWICImagingFactory \_

Função de proxy para o método [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_guidContainerFormat * \[ in\]
</dt> <dd>

Tipo: **REFGUID**

O GUID para o formato de contêiner desejado.

</dd> <dt>

*pguidVendor* \[ em, opcional\]
</dt> <dd>

Tipo: **const GUID \** _

O GUID do fornecedor para o codificador.

</dd> <dt>

_ppIEncoder * \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




