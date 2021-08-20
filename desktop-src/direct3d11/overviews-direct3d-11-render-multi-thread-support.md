---
title: Como verificar se há suporte para driver
description: Este tópico mostra como determinar se os recursos de multithreading (incluindo a criação de recursos e listas de comandos) têm suporte para aceleração de hardware.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30915f8cdd19e59f5841a77fc93946df8e3bc6c8df37f53217b4afac2be0f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912847"
---
# <a name="how-to-check-for-driver-support"></a>Como verificar se há suporte para driver

Este tópico mostra como determinar se os [](overviews-direct3d-11-render-multi-thread-intro.md) recursos de multithreading (incluindo a criação de recursos e listas de comandos [)](overviews-direct3d-11-render-multi-thread-command-list.md)têm suporte para aceleração de hardware.

Recomendamos que os aplicativos verifiquem se há suporte a hardware gráfico de multithreading. Se o driver e o hardware de gráficos não deem suporte à criação de objetos multithread, o desempenho poderá ser limitado das seguintes maneiras:

-   Criar vários objetos (mesmo de tipos diferentes) ao mesmo tempo pode ser limitado.
-   A criação de um objeto ao renderizar comandos gráficos usando [um contexto imediato](overviews-direct3d-11-render-multi-thread-render.md) pode ser limitada. Por exemplo, se o hardware não dá suporte a multithreading, um aplicativo deve evitar criar em um thread em segundo plano um objeto que requer muito tempo para criar. Uma operação de criação que leva muito tempo pode bloquear a renderização imediata do contexto e aumentar o risco de um stutter de taxa de quadros visual.

O runtime dá suporte a multithreading e listas de comandos, independentemente do suporte a driver e hardware; se não houver suporte de driver e hardware para multithreads ou listas de comandos, o runtime emulará a funcionalidade. Para obter mais informações sobre multithreading, consulte [Introdução ao Multithreading no Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**Para verificar se há suporte para driver para multithreading:**

1.  Inicialize um objeto de interface [**ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) Por padrão, multithreading está habilitado.
2.  Chame [**ID3D11Device::CheckFeatureSupport.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Passe o valor **D3D11 \_ FEATURE \_ THREADING** para o parâmetro Feature, passe a estrutura [**D3D11 \_ FEATURE DATA \_ \_ THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) para o parâmetro *pFeatureSupportData* e passe o tamanho da estrutura **D3D11 \_ FEATURE DATA \_ \_ THREADING** para o parâmetro *FeatureSupportDataSize.* 
3.  Se o método [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) for bem-sucedido, a estrutura [**D3D11 FEATURE DATA THREADING que você passou na etapa anterior será inicializada com informações sobre o suporte a \_ multithreading. \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading)
    -   Se **DriverConcurrentCreates** for **TRUE,** um driver poderá criar mais de um recurso ao mesmo tempo (simultaneamente) em threads diferentes.

        Se **DriverCommandLists for** **TRUE,** o driver será compatível com listas de comandos. Ou seja, os comandos de renderização emitidos por um contexto imediato podem ser simultâneos com a criação de objeto em threads separados com baixo risco de um stutter de taxa de quadros.

    -   Se **DriverConcurrentCreates** for **FALSE,** um driver não dá suporte à criação simultânea, o que significa que a quantidade de simultrreidade possível é extremamente limitada. O hardware gráfico não pode criar objetos de tipos diferentes em threads diferentes de forma simultana. Além disso, o hardware gráfico não pode usar um contexto imediato para emitir comandos de renderização enquanto o hardware gráfico tenta criar um recurso em outro thread.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




