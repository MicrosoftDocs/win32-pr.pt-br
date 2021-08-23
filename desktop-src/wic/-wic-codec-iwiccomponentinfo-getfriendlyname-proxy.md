---
description: Função de proxy para o método getfriendlyname.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Função IWICComponentInfo_GetFriendlyName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5af41c00945550fc9e833b9324e22f522aa7a5e73dacd109d76159d5dd0173db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965245"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>\_Função de proxy IWICComponentInfo Getfriendlyname \_

Função de proxy para o método [**Getfriendlyname**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Ponteiro para este objeto [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchFriendlyName* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho do buffer *wzFriendlyName* .

</dd> <dt>

*wzFriendlyName* \[ entrada, saída\]
</dt> <dd>

Tipo: **WCHAR \***

Um ponteiro que recebe o nome amigável do componente.

A cadeia de caracteres retornada é específica da localidade, 1033 por padrão.

</dd> <dt>

*pcchActual* \[ fora\]
</dt> <dd>

Tipo: **uint \***

Um ponteiro que recebe o comprimento real do nome amigável do componente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, somente aplicativos do Windows Vista \[ desktop\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




