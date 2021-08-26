---
description: Função proxy para o método GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056596"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>Função \_ proxy GetChannelMask IWICPixelFormatInfo \_

Função proxy para o [**método GetChannelMask.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Ponteiro para este [**objeto IWICPixelFormatInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)

</dd> <dt>

*uiChannelIndex* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O índice para a máscara de canal a ser recuperada.

</dd> <dt>

*cbMaskBuffer* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tamanho do *buffer pbMaskBuffer.*

</dd> <dt>

*pbMaskBuffer* \[ in, out\]
</dt> <dd>

Tipo: **BYTE \***

Ponteiro para o buffer de máscara.

</dd> <dt>

*pcbActual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

O tamanho real do buffer necessário para obter a máscara de canal.

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



 

 




