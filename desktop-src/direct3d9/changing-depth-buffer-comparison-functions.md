---
description: Por padrão, quando o teste de profundidade é executado em uma superfície de renderização, o sistema Direct3D atualiza a superfície de destino de renderização se o valor de profundidade correspondente (z ou w) para cada ponto for menor que o valor no buffer de profundidade.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Alterando funções de comparação de buffer de profundidade (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646540"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Alterando funções de comparação de buffer de profundidade (D3D9)

Por padrão, quando o teste de profundidade é executado em uma superfície de renderização, o sistema Direct3D atualiza a superfície de destino de renderização se o valor de profundidade correspondente (z ou w) para cada ponto for menor que o valor no buffer de profundidade. Em um aplicativo C++, você altera como o sistema executa comparações em valores de profundidade chamando o método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) com o parâmetro *State* definido como D3DRS \_ ZFUNC. O parâmetro *Value* deve ser definido como um valor no tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
