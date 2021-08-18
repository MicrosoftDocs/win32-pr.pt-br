---
description: Função proxy para criar um IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: WICCreateColorContext_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e525b86403e1bcee8b25aba90d2af3850dbc06964aab4ae89feadf5eb0678f41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347376"
---
# <a name="wiccreatecolorcontext_proxy-function"></a>Função proxy WICCreateColorContext \_

Função proxy para criar [**um IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

Ponteiro para este [**objeto IWICImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)

</dd> <dt>

*ppIColorContext* 
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, Windows aplicativos da área de trabalho do Vista \[\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




