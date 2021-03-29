---
title: Criação de pool de blocos
description: Um pool de blocos é criado por meio da API CreateBuffer ID3D11Device passando o \_ sinalizador de pool de blocos diversos do recurso D3D11 \_ \_ \_ no membro MiscFlags \_ da \_ estrutura Desc do buffer D3D11 para a qual o parâmetro pDesc aponta.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988496"
---
# <a name="tile-pool-creation"></a>Criação de pool de blocos

Um pool de blocos é criado por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando o sinalizador de [**\_ \_ \_ \_ pool de blocos diversos do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) no membro **MiscFlags** da estrutura [**\_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para a qual o parâmetro *pDesc* aponta.

Os apps podem criar um ou mais pools de blocos por dispositivo Direct3D. O tamanho total de cada pool de blocos é restrito ao limite de tamanho de recursos do Direct3D 11, que é aproximadamente 1/4 da RAM da GPU (unidade de processamento gráfico).

Um pool de blocos é composto por blocos de 64 KB, mas o sistema operacional (driver de vídeo) gerencia o pool inteiro como uma ou mais alocações em segundo plano – a divisão não fica visível para os aplicativos. Os recursos ao lado do bloco definem o conteúdo apontando para blocos dentro de um pool de peças. É feito o desmapeamento de um bloco de um recurso de mosaico, apontando o bloco para **nulo**. Esses blocos não mapeados têm regras sobre o comportamento de leituras ou gravações. Para obter informações, consulte [controle de risco versus recursos do pool de blocos](hazard-tracking-versus-tile-pool-resources.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamentos estão em um pool de blocos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




