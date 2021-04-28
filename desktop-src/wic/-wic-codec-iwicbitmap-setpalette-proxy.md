---
description: Função IWICBitmap_SetPalette_Proxy function-proxy para o método SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Função IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086404"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a>\_Função de proxy SetPalette IWICBitmap \_

Função de proxy para o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Ponteiro para este objeto [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*pIPalette* \[ no\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

A paleta a ser usada para conversão.

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



 

 




