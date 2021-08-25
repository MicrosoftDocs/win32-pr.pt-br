---
description: Função proxy para o método CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e9c847680a93cb245b0e5d4247cb60b82629ea82eba12313dbcff7303dcce707
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772336"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>Função proxy IWICBitmapSource \_ CopyPixels \_

Função proxy para o [**método CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Ponteiro para este [**objeto IWICBitmapSource.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)

</dd> <dt>

*prc* \[ Em\]
</dt> <dd>

Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

O retângulo a ser copiado. Um valor NULL especifica todo o bitmap.

</dd> <dt>

*cbStride* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O avanço do bitmap

</dd> <dt>

*cbBufferSize* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tamanho do buffer.

</dd> <dt>

*pbBuffer* \[ out\]
</dt> <dd>

Tipo: **BYTE \***

Um ponteiro para o buffer.

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



 

 




