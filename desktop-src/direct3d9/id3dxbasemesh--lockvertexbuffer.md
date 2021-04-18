---
description: Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'Método ID3DXBaseMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815467"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>Método ID3DXBaseMesh:: LockVertexBuffer

Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado. Para esse método, os sinalizadores válidos são:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ nenhuma \_ \_ atualização suja
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOoverwrite

Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Ponteiro void para um buffer que contém os dados do vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Ao trabalhar com buffers de vértice, você tem permissão para fazer várias chamadas de bloqueio; no entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio. Chamadas de DrawPrimitive não terão sucesso com qualquer contagem de bloqueios pendentes em qualquer buffer de vértice definido no momento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
