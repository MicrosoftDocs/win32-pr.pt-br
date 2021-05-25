---
description: Protótipo de função usado por D3DXComputeIMTFromSignal para descrever um sinal definido pelo usuário no espaço u,v de uma malha de entrada. A função avalia um sinal de procedimento da dimensão uSignalDimension na coordenada u,v fornecida.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342831"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Protótipo de função usado por [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para descrever um sinal definido pelo usuário no espaço u,v de uma malha de entrada. A função avalia um sinal de procedimento da dimensão uSignalDimension na coordenada u,v fornecida.

## <a name="syntax"></a>Sintaxe


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Parâmetros

\[in \] uv – um ponteiro para um vetor que contém a coordenada de textura do vértice.

\[em uPrimitiveId – o índice do triângulo de entrada na malha para o \] qual o sinal deve ser calculado.

\[em uSignalDimension – o número de floats a armazenar na matriz de dados \] de sinal (pfSignalOut).

\[em \] pUserData – o ponteiro pUserData passado para [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut – uma matriz de floats, que contém os dados de sinal.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK.

## <a name="remarks"></a>Comentários

Especifique a convenção de chamada Tipos de [**Dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



| Requisito               | Valor            |
|----------------|-------------|
| parâmetro         | d3dx9mesh.h |
| Bibliotecas de importação | d3dx9.lib   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
