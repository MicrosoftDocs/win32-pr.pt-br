---
description: Protótipo de função usado pelo D3DXComputeIMTFromSignal para descrever um sinal definido pelo usuário em um u, espaço v de malha de entrada. A função avalia um sinal de procedimento de uSignalDimension de dimensão na coordenada u, v fornecida.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808297"
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

Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



|                |             |
|----------------|-------------|
| parâmetro         | d3dx9mesh. h |
| Bibliotecas de importação | d3dx9. lib   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
