---
description: Recupera as opções de malha habilitadas para esta malha no momento da criação.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'Método ID3DXBaseMesh:: getoptions (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b8ed6281e1418246027a05f281ef5c01d8fbe757a8bd88d2bf6f44ca41ed1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121758"
---
# <a name="id3dxbasemeshgetoptions-method"></a>Método ID3DXBaseMesh:: getoptions

Recupera as opções de malha habilitadas para esta malha no momento da criação.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Retorna uma combinação de um ou mais dos sinalizadores a seguir, indicando as opções habilitadas para esta malha no momento da criação.



| Valor                   | Descrição                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 bits         | Use índices de 32 bits.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Use o \_ sinalizador de uso D3DUSAGE DONOTCLIP para os buffers de vértice e de índice.                                                                                                                             |
| D3DXMESH \_ dinâmico       | Equivalente a especificar o D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Use o \_ sinalizador de uso D3DUSAGE RTPATCHES para os buffers de vértice e de índice.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | A especificação desse sinalizador faz com que o vértice e o buffer do índice da malha sejam criados com o \_ sinalizador D3DUSAGE NPATCHES. Isso será necessário se o objeto de malha for renderizado usando o aprimoramento de N-patch. |
| \_Gerenciado D3DXMESH       | Equivalente a especificar o D3DXMESH \_ VB \_ gerenciado e o D3DXMESH \_ IB \_ gerenciados.                                                                                                                   |
| Pontos de D3DXMESH \_        | Use o \_ sinalizador de uso de pontos D3DUSAGE para os buffers de vértice e de índice.                                                                                                                                |
| D3DXMESH \_ IB \_ Dynamic   | Use o \_ sinalizador de uso dinâmico D3DUSAGE para buffers de índice.                                                                                                                                          |
| D3DXMESH \_ IB \_ gerenciado   | Use a \_ classe de memória gerenciada D3DPOOL para buffers de índice.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Use a \_ classe de memória D3DPOOL SYSTEMMEM para buffers de índice.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Use o \_ sinalizador de uso de WRITEONLY D3DUSAGE para buffers de índice.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM e D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ Dynamic   | Use o \_ sinalizador de uso dinâmico D3DUSAGE para buffers de vértice.                                                                                                                                         |
| Gerenciado por D3DXMESH \_ VB \_   | Use a \_ classe de memória gerenciada D3DPOOL para buffers de vértice.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Use a \_ classe de memória D3DPOOL SYSTEMMEM para os buffers de vértice.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Use o \_ sinalizador de uso de WRITEONLY D3DUSAGE para buffers de vértice.                                                                                                                                       |
| \_WRITEONLY D3DXMESH     | Equivalente a especificar ambos D3DXMESH \_ VB \_ WRITEONLY e D3DXMESH \_ IB \_ WriteOnly.                                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
