---
description: Protótipo de função usado pelo D3DXComputeIMTFromSignal para descrever um sinal definido pelo usuário em um u, espaço v de malha de entrada. A função avalia um sinal de procedimento de uSignalDimension de dimensão na coordenada u, v fornecida.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e4f6ffaa4c844e755d489aae52dd13b8390da1145734d50f5865bbe0e3cfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728503"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Protótipo de função usado pelo [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para descrever um sinal definido pelo usuário em um u, espaço v de malha de entrada. A função avalia um sinal de procedimento de uSignalDimension de dimensão na coordenada u, v fornecida.

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

\[em \] UV-um ponteiro para um vetor que contém a coordenada de textura de vértice.

\[em \] uPrimitiveId-o índice do triângulo de entrada na malha para a qual o sinal deve ser calculado.

\[em \] uSignalDimension-o número de floats para armazenar na matriz de dados de sinal (pfSignalOut).

\[em \] pUserData-o ponteiro pUserData passado para [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut-uma matriz de floats que contém os dados de sinal.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK.

## <a name="remarks"></a>Comentários

certifique-se de especificar a convenção de chamada de [**tipos de dados Windows**](../winprog/windows-data-types.md) ao declarar a função de chamada de retorno. Caso contrário, podem ocorrer estouros de pilha.



| Requisito               | Valor            |
|----------------|-------------|
| parâmetro         | d3dx9mesh. h |
| Bibliotecas de importação | d3dx9. lib   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
