---
description: Função de retorno de chamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791410"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Função de retorno de chamada para UVAtlas.

## <a name="syntax"></a>Sintaxe


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parâmetros

\[out \] fPercentDone-número de ponto flutuante entre 0 e 1,0 que representa a porcentagem de cálculos concluídos (entre 0 e 100 por cento).

\[no \] lpUserContext-pointer para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor interromperá o simulador.

## <a name="remarks"></a>Comentários

Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



|                          |             |
|--------------------------|-------------|
| parâmetro                   | d3dx9mesh. h |
| Bibliotecas de importação           | d3dx9. lib   |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
