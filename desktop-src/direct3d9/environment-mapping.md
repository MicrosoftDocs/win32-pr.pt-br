---
description: O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o rastreamento de raio.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapeamento de ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a07d53028e200d273206f149ea12c07afa6dbc4ad47f8232e64cddf7582a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122214"
---
# <a name="environment-mapping-direct3d-9"></a>Mapeamento de ambiente (Direct3D 9)

O mapeamento de ambiente é uma técnica que simula superfícies altamente reflexivas sem usar o rastreamento de raio. Na prática, o mapeamento de ambiente aplica um mapa de textura especial que contém uma imagem da cena em torno de um objeto para o próprio objeto. O resultado aproxima a aparência de uma superfície reflexiva, próxima o suficiente para enganar o olho, sem incorrer em nenhum dos cálculos complexos envolvidos no rastreamento de raio.

A ilustração a seguir demonstra um tipo de mapeamento de ambiente chamado mapeamento de ambiente esférico. Para obter detalhes, consulte [Mapeamento de ambiente esférico](spherical-environment-mapping.md).

![ilustração de um bule com uma textura aplicada que reflete o ambiente](images/spheremapped-teapot.png)

O bule nessa imagem parece refletir seu ambiente; essa é, na verdade, uma textura que está sendo aplicada ao objeto . Como o mapeamento de ambiente usa uma textura, combinada com coordenadas de textura especialmente computadas, ela pode ser executada em tempo real.

Esta seção fornece informações sobre como executar dois tipos comuns de mapeamento de ambiente com o Direct3D. Há muitos tipos de mapeamento de ambiente em uso em todo o setor gráfico, mas os tópicos a seguir são destinados às duas formas mais comuns: mapeamento de ambiente cúbica e mapeamento de ambiente esférico.

-   [Mapeamento de ambiente cúbica](cubic-environment-mapping.md)
-   [Mapeamento de ambiente esférico](spherical-environment-mapping.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 



