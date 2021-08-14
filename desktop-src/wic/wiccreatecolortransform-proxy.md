---
description: Cria um objeto de transformação de cor que implementa IWICColorTransform. Este objeto COM dá suporte ao modelo de objeto de thread livre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Função WICCreateColorTransform_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 89c7476bc32546f0a9fe77a8731f239702c6a2a874dbfb830b9d4bbafbd872b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709213"
---
# <a name="wiccreatecolortransform_proxy-function"></a>\_Função de proxy WICCreateColorTransform

Cria um objeto de transformação de cor que implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Este objeto COM dá suporte ao modelo de objeto de thread livre.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIColorTransform* \[ fora\]
</dt> <dd>

A transformação de cor criada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
