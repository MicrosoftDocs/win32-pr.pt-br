---
description: Função de proxy para o método InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: Função IWICStream_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764175"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>\_Função de \_ proxy IWICStream InitializeFromMemory

Função de proxy para o método [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _

Ponteiro para este objeto [_ *IWICStream* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .

</dd> <dt>

*pbBuffer* \[ no\]
</dt> <dd>

Tipo: **byte \** _

Ponteiro para o buffer usado para inicializar o fluxo.

</dd> <dt>

_cbBufferSize * \[ in\]
</dt> <dd>

Tipo: **DWORD**

O tamanho do buffer.

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



 

 




