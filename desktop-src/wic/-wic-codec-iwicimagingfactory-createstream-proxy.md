---
description: Função de proxy para o método CreateStream.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Função IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814109"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a>\_Função de proxy CreateStream IWICImagingFactory \_

Função de proxy para o método [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIWICStream * \[ out\]
</dt> <dd>

Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




