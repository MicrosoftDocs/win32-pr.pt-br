---
description: Função de proxy para o método InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: Função IWICPalette_InitializeCustom_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811729"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a>\_Função de \_ proxy IWICPalette InitializeCustom

Função de proxy para o método [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Ponteiro para este objeto [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*pColors* \[ no\]
</dt> <dd>

Tipo: **WICColor \** _

Ponteiro para a matriz de cores.

</dd> <dt>

_colorCount * \[ in\]
</dt> <dd>

Tipo: **uint**

O número de cores em *pColors*.

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



 

 




