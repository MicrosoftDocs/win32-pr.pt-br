---
description: Inicializa um IWICColorTransform com um IWICBitmapSource e o transforma de um IWICColorContext em outro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: fcfe124d03e9ad41edb49554613bc18b2cd15818b3f52db7ca368e27f5c4fcc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841366"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Função Inicializar Proxy IWICColorTransform \_ \_

Inicializa um [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) com [**um IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e o transforma de [**um IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) em outro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIColorTransform* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

A transformação de cor a ser inicializada.

</dd> <dt>

*pIBitmapSource* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

A origem do bitmap usada para inicializar a transformação de cor.

</dd> <dt>

*pIContextSource* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

A origem do contexto de cor.

</dd> <dt>

*pIContextDest* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

O destino do contexto de cor.

</dd> <dt>

*pixelFmtDest* \[ Em\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

O GUID do formato de pixel desejado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




