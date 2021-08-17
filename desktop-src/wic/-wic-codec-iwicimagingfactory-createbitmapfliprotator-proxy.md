---
description: Função de proxy para o método CreateBitmapFlipRotator.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: Função IWICImagingFactory_CreateBitmapFlipRotator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9f54d4f38b84ad9e91a6b7aca6696e54fdf07d9f1b331c13b611e81a1fbfa8db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088338"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateBitmapFlipRotator

Função de proxy para o método [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIBitmapFlipRotator* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, somente aplicativos do Windows Vista \[ desktop\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




