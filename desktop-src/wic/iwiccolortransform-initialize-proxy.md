---
description: Inicializa um IWICColorTransform com um IWICBitmapSource e o transforma de um IWICColorContext para outro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Função IWICColorTransform_Initialize_Proxy
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
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782517"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Função de proxy de \_ inicialização IWICColorTransform \_

Inicializa um [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) com um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e o transforma de um [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para outro.

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

*pIColorTransform* \[ no\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

A transformação de cor a ser inicializada.

</dd> <dt>

*pIBitmapSource* \[ no\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

A origem do bitmap usada para inicializar a transformação de cor.

</dd> <dt>

*pIContextSource* \[ no\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

A origem do contexto de cor.

</dd> <dt>

*pIContextDest* \[ no\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

O destino do contexto de cor.

</dd> <dt>

*pixelFmtDest* \[ no\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

O GUID do formato de pixel desejado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 




