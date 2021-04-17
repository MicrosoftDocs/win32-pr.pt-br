---
description: Obtém um IMemoryBuffer como uma matriz de bytes.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Método IMemoryBufferByteAccess:: GetBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782783"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>Método IMemoryBufferByteAccess:: GetBuffer

Obtém um [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como uma matriz de bytes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém os dados do buffer.

</dd> <dt>

*capacidade* \[ do fora\]
</dt> <dd>

O número de bytes na matriz retornada

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando [**memorybuffer já:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) é chamado, o código que usa esse buffer deve definir o ponteiro de *valor* como NULL.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
