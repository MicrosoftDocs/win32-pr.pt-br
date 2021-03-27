---
title: Usando vinculação de sombreador
description: Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641753"
---
# <a name="using-shader-linking"></a>Usando vinculação de sombreador

Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução. A vinculação de sombreador tem suporte a partir de Windows 8.1.

**Objetivo:** Saiba como usar a vinculação de sombreador.

## <a name="prerequisites"></a>Pré-requisitos

Partimos do princípio de que você conhece C++. Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.

**Tempo total para conclusão:** 60 minutos.

## <a name="where-to-go-from-here"></a>Para onde ir a partir de agora

Consulte também [APIs de compilador do HLSL](dx-graphics-d3dcompiler-reference.md).

Nós lhe mostramos como:

-   Compilar o código do sombreador
-   Carregar o código compilado em uma biblioteca de sombreador
-   Associar os recursos dos slots de origem aos slots de destino
-   Construir FLGs (função-vinculação-grafos) para sombreadores
-   Vincular grafos de sombreador com uma biblioteca de sombreador para produzir um blob de sombreador que o tempo de execução do Direct3D pode usar

Em seguida, criamos uma biblioteca de sombreador e ligamos os recursos dos slots de origem aos slots de destino.

[Empacotando uma biblioteca de sombreador](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Elementos gráficos do Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 