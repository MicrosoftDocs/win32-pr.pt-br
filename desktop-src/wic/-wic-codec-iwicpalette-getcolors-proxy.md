---
description: Função de proxy para o método getcolors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Função IWICPalette_GetColors_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170459"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>\_Função de proxy IWICPalette Getcolors \_

Função de proxy para o método [**Getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Ponteiro para este objeto [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*colorCount* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho da matriz *pColors* .

</dd> <dt>

*pColors* \[ fora\]
</dt> <dd>

Tipo: **WICColor \** _

Ponteiro que recebe as cores da paleta.

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

Tipo: **uint \** _

O tamanho real necessário para obter as cores da paleta.

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



 

 




