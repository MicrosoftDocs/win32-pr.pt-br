---
description: Função IWICBitmapFlipRotator_Initialize_Proxy function-proxy para o método Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: Função IWICBitmapFlipRotator_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091154"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a>Função de proxy de \_ inicialização IWICBitmapFlipRotator \_

Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***

Ponteiro para este objeto [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

</dd> <dt>

*pISource* \[ no\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

A origem do bitmap de entrada.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**

O [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para inverter ou girar a imagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




