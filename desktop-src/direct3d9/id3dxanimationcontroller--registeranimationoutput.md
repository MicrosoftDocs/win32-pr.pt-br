---
description: Adiciona uma saída de animação ao controlador de animação e registra ponteiros para transformações de escala, rotação e tradução (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: Método ID3DXAnimationController::RegisterAnimationOutput (D3dx9 multimídia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc48eb9f2fd6ee5fee6c04936801997145a5ea21542b9b5ff8ec6d257eee80e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987816"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>Método ID3DXAnimationController::RegisterAnimationOutput

Adiciona uma saída de animação ao controlador de animação e registra ponteiros para transformações de escala, rotação e tradução (SRT).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da saída da animação.

</dd> <dt>

*pMatrix* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma [**estrutura D3DXMATRIX que**](d3dxmatrix.md) contém dados de transformação SRT. Pode ser **NULL.**

</dd> <dt>

*pScale* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para um [**vetor D3DXVECTOR3**](d3dxvector3.md) que descreve a escala do conjunto de animação. Pode ser **NULL.**

</dd> <dt>

*pRotation* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para um [**quatternion D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação do conjunto de animação. Pode ser **NULL.**

</dd> <dt>

*pTranslation* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para um [**vetor D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução do conjunto de animação. Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se a saída da animação já estiver registrada, o pMatrix será preenchido com os dados de transformação de entrada.

Conjuntos de animação criados [**com D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registram automaticamente todos os conjuntos de animação carregados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
