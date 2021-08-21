---
description: Função de retorno de chamada para simulação e compactação de PRT (transferência de radiante preputada).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799329"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Função de retorno de chamada para simulação e compactação de PRT (transferência de radiante preputada).

## <a name="syntax"></a>Sintaxe


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parâmetros

fPercentDone-número de ponto flutuante entre 0 e 1,0 que representa a porcentagem de cálculos concluídos (entre 0 e 100 por cento).

lpUserContext-ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor interromperá o simulador.

## <a name="remarks"></a>Comentários

certifique-se de especificar a convenção de chamada de [**tipos de dados Windows**](../winprog/windows-data-types.md) ao declarar a função de chamada de retorno. Caso contrário, podem ocorrer estouros de pilha.



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3dx9mesh. h |
| Bibliotecas de importação           | d3dx9. lib   |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
