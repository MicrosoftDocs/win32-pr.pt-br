---
description: Função de proxy para o método getmimetypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: Função IWICBitmapCodecInfo_GetMimeTypes_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501616"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a>\_Função de proxy IWICBitmapCodecInfo Getmimetypes \_

Função de proxy para o método [**Getmimetypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Ponteiro para este objeto [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchMimeTypes* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho do buffer de tipos MIME.

</dd> <dt>

*wzMimeTypes* \[ fora\]
</dt> <dd>

Tipo: **WCHAR \** _

Um ponteiro que recebe os tipos MIME associados ao codec.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Tipo: **uint \** _

O tamanho real do buffer necessário para recuperar todos os tipos MIME associados ao codec.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




