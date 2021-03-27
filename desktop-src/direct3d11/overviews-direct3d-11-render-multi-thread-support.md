---
title: Como verificar o suporte ao driver
description: Este tópico mostra como determinar se os recursos de multithreading (incluindo a criação de recursos e as listas de comandos) têm suporte para aceleração de hardware.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988507"
---
# <a name="how-to-check-for-driver-support"></a>Como: verificar o suporte de driver

Este tópico mostra como determinar se os recursos de multithreading (incluindo a [criação de recursos](overviews-direct3d-11-render-multi-thread-intro.md) e as [listas de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)) têm suporte para aceleração de hardware.

Recomendamos que os aplicativos verifiquem o suporte a hardware de gráficos de multithreading. Se o driver e o hardware de gráficos não suportarem a criação de objetos multithread, o desempenho poderá ser limitado das seguintes maneiras:

-   A criação de vários objetos (mesmo de tipos diferentes) ao mesmo tempo pode ser limitada.
-   Criar um objeto ao renderizar comandos gráficos usando um [contexto imediato](overviews-direct3d-11-render-multi-thread-render.md) pode ser limitado. Por exemplo, se o hardware não oferecer suporte a multithreading, um aplicativo deverá evitar a criação em um thread em segundo plano um objeto que requer muito tempo para ser criado. Uma operação de criação que leva muito tempo pode bloquear a renderização imediata do contexto e aumentar o risco de uma stutter de taxa de quadros Visual.

O tempo de execução dá suporte a vários threads e listas de comandos, independentemente do suporte a driver e hardware; Se não houver suporte de driver e de hardware para vários threads ou listas de comandos, o tempo de execução emulará a funcionalidade. Para obter mais informações sobre multithreading, consulte [introdução ao multithreading no Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**Para verificar o suporte de driver para multithreading:**

1.  Inicializar um objeto de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) . Por padrão, o multithreading está habilitado.
2.  Chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Passe o valor de **\_ \_ Threading do recurso D3D11** para o parâmetro *Feature* , passe a estrutura de [**Threading de \_ dados do recurso \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) para o parâmetro *pFeatureSupportData* e passe o tamanho da estrutura de **Threading de \_ dados do recurso \_ \_ D3D11** para o parâmetro *FeatureSupportDataSize* .
3.  Se o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) for bem-sucedido, a estrutura de threading de dados de recursos do D3D11 que você passou na etapa anterior será inicializada com informações sobre o suporte a multithreading. [**\_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading)
    -   Se **DriverConcurrentCreates** for **true**, um driver poderá criar mais de um recurso ao mesmo tempo (simultaneamente) em threads diferentes.

        Se **DriverCommandLists** for **true**, o driver dará suporte a listas de comandos. Ou seja, os comandos de renderização emitidos por um contexto imediato podem ser simultâneos com a criação de objeto em threads separados com baixo risco de um stutter de taxa de quadros.

    -   Se **DriverConcurrentCreates** for **false**, um driver não oferecerá suporte à criação simultânea, o que significa que a quantidade de simultaneidade possível é extremamente limitada. O hardware de gráficos não pode criar objetos de tipos diferentes em threads diferentes simultanueously. Além disso, o hardware de gráficos não pode usar um contexto imediato para emitir comandos de renderização enquanto o hardware de gráficos tenta criar um recurso em outro thread.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




