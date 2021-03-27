---
title: Arquitetura de memória unificada
description: Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916023"
---
# <a name="unified-memory-architecture"></a>Arquitetura de memória unificada

Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.

Um booliano, definido pelo driver, pode ser lido na estrutura [**D3D11 de \_ dados do recurso \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) para determinar se o hardware dá suporte a uma.

Os aplicativos em execução em uma pode querer ter mais recursos com acesso à CPU habilitado do que se não estiverem disponíveis. Uma a permite que os aplicativos evitem copiar dados de recursos, em vez de permanecerem eficientes exclusivamente para adaptadores de elementos gráficos não pertencentes a uma. [Recursos do Direct3D 11,3](direct3d-11-3-features.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




