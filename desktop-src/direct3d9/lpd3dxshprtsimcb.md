---
description: Função de retorno de chamada para simulação e compactação de PRT (Transferência de Radiance Pré-comutada).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342801"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Função de retorno de chamada para simulação e compactação de PRT (Transferência de Radiance Pré-comutada).

## <a name="syntax"></a>Sintaxe


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parâmetros

fPercentDone – número de ponto flutuante entre 0 e 1,0 que representa o percentual de cálculos concluídos (entre 0 e 100%).

lpUserContext – ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

## <a name="return-value"></a>Valor Retornado

Essa função deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor interromperá o simulador.

## <a name="remarks"></a>Comentários

Especifique a convenção de chamada Tipos de [**Dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3dx9mesh.h |
| Bibliotecas de importação           | d3dx9.lib   |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
