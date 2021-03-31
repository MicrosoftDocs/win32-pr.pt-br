---
description: O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o Ray tracing.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapeamento de ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645762"
---
# <a name="environment-mapping-direct3d-9"></a>Mapeamento de ambiente (Direct3D 9)

O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o Ray tracing. Na prática, o mapeamento de ambiente aplica um mapa de textura especial que contém uma imagem da cena em torno de um objeto ao próprio objeto. O resultado aproxima a aparência de uma superfície reflexiva, perto o suficiente para enganar o olho, sem incorrer em nenhum cálculo complexo envolvido no rastreamento de Ray.

A ilustração a seguir demonstra um tipo de mapeamento de ambiente chamado de mapeamento de ambiente esférico. Para obter detalhes, consulte [mapeamento de ambiente esférico](spherical-environment-mapping.md).

![ilustração de um bule com uma textura aplicada que reflete os arredores](images/spheremapped-teapot.png)

O bule nessa imagem parece refletir seu ambiente; na verdade, essa é uma textura que está sendo aplicada ao objeto. Como o mapeamento de ambiente usa uma textura, combinada com coordenadas de textura especialmente computadas, ela pode ser executada em tempo real.

Esta seção fornece informações sobre como executar dois tipos comuns de mapeamento de ambiente com o Direct3D. Há muitos tipos de mapeamento de ambiente em uso em todo o setor de gráficos, mas os seguintes tópicos visam os dois formulários mais comuns: mapeamento de ambiente cúbico e mapeamento de ambiente esférico.

-   [Mapeamento de ambiente cúbico](cubic-environment-mapping.md)
-   [Mapeamento de ambiente esférico](spherical-environment-mapping.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 



