---
description: Função de retorno de chamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4473134d7ecf98c50d0c3a69085e7f46344d1d57ff2650c1adbc54c43dba266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458707"
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

\[out fPercentDone – número de ponto flutuante entre 0 e 1,0 que representa o percentual de cálculos \] concluídos (entre 0 e 100%).

\[em lpUserContext – ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de \] chamada.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor interromperá o simulador.

## <a name="remarks"></a>Comentários

Especifique a convenção [**de chamada Windows tipos**](../winprog/windows-data-types.md) de dados ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3dx9mesh.h |
| Bibliotecas de importação           | d3dx9.lib   |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
