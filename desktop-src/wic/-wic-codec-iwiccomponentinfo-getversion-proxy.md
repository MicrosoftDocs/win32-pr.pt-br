---
description: Função proxy para o método GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5a781aacbe0b5b9dd35a94c2ce906ee546e0b1da6b426a6848b6aafed2721cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965215"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>Função \_ proxy GetVersion IWICComponentInfo \_

Função proxy para o [**método GetVersion.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Ponteiro para este [**objeto IWICComponentInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchVersion* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tamanho do buffer *wzVersion.*

</dd> <dt>

*wzVersion* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Um ponteiro que recebe uma cadeia de caracteres invariável de cultura da versão do componente.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Um ponteiro que recebe o comprimento real da versão do componente.

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



 

 




