---
description: Função proxy para o método GetAuthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c83d42f499c8f821f5b342f08749a2167aac9cc61334fe2fc2d9e9134b5e2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206667"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>Função \_ proxy GetAuthor IWICComponentInfo \_

Função proxy para o [**método GetAuthor.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
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

*cchAuthor* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tamanho do *buffer wzAuthor.*

</dd> <dt>

*wzAuthor* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Um ponteiro que recebe o nome do autor do componente.

A cadeia de caracteres retornada é específica da localidade, 1033 por padrão.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Um ponteiro que recebe o comprimento real do nome dos autores do componente.

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



 

 




