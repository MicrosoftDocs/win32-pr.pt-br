---
title: Usando a vinculação do sombreador
description: Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de executar.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f382596f3839460943fdbefe5687c4e7b18401db016ad3f834284e994217b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742276"
---
# <a name="using-shader-linking"></a>Usando a vinculação do sombreador

Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de executar. Há suporte para a vinculação do sombreador a partir do Windows 8.1.

**Objetivo:** Saiba como usar a vinculação de sombreador.

## <a name="prerequisites"></a>Pré-requisitos

Partimos do princípio de que você conhece C++. Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.

**Tempo total para conclusão:** 60 minutos.

## <a name="where-to-go-from-here"></a>Para onde ir a partir de agora

Consulte também APIs do [compilador HLSL.](dx-graphics-d3dcompiler-reference.md)

Nós lhe mostramos como:

-   Compilar o código do sombreador
-   Carregar o código compilado em uma biblioteca de sombreadores
-   Vincular os recursos dos slots de origem aos slots de destino
-   Construir flGs (grafos de vinculação de função) para sombreadores
-   Vincular grafos de sombreador com uma biblioteca de sombreador para produzir um blob de sombreador que o runtime do Direct3D pode usar

Em seguida, fazemos uma biblioteca de sombreador e vinculamos recursos de slots de origem a slots de destino.

[Empacotando uma biblioteca de sombreador](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Elementos gráficos do Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 