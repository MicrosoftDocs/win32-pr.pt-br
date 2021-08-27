---
description: Função de proxy para o método CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: Função IWICImagingFactory_CreatePalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 23f970acdd6166547322714cdcf5cd5cd8c4d0875616f5bbe692a02d06f8a8fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056606"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a>\_Função de proxy CreatePalette IWICImagingFactory \_

Função de proxy para o método [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIPalette* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).

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



 

 




