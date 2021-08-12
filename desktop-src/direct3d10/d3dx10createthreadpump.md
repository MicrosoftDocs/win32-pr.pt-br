---
description: Criar uma bomba de thread.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Função D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 99b5766625f2a269d1fb36e9e808c206d0e3040419f505622ccfe1e27ca4bcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541051"
---
# <a name="d3dx10createthreadpump-function"></a>Função D3DX10CreateThreadPump

Criar uma bomba de thread.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cIoThreads* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de threads de e/s a serem criados. Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.

</dd> <dt>

*cProcThreads* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de threads de processo a serem criados. Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.

</dd> <dt>

*ppThreadPump* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

A bomba de thread criada. Consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Uma bomba de thread é um objeto com uso intensivo de recursos. Somente uma bomba de thread deve ser criada por aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
