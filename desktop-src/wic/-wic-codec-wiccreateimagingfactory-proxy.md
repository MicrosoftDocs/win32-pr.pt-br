---
description: Função de proxy para criar o IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Função WICCreateImagingFactory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765653"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>\_Função de proxy WICCreateImagingFactory

Função de proxy para criar o [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SDKVersion* \[ no\]
</dt> <dd>

Tipo: **uint**

</dd> <dt>

*ppIImagingFactory* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função é um auxiliar para criar uma fábrica de WIC para a vinculação de DLL explícita, que era necessária para o Windows XP. No uso normal, você usaria [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em vez disso (consulte [fábricas de classe da API do WIC](./-wic-api.md#class-factories)), já que isso é sempre incluído em todas as versões mais recentes do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>WindowsCodecs. lib</dt> </dl> |



 

