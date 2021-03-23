---
title: Heaps de descritor visíveis do sombreador
description: Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104204"
---
# <a name="shader-visible-descriptor-heaps"></a>Heaps de descritor visíveis do sombreador

Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.

-   [Visão geral](#overview)
-   [Um exemplo](#an-example)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Os heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor vêm em alguns tipos: um tipo de heap, \_ heap de descritor de D3D12 SRV \_ UAV \_ cbv \_ \_ , pode conter exibições de recursos de sombreador, exibições de acesso não ordenadas e exibições de buffer constantes, todas combinadas. Qualquer local especificado no heap pode ser qualquer um dos tipos de descritores listados. Outro tipo de heap, \_ amostra de tipo de heap de descritor de D3D12 \_ \_ \_ , só armazena amostras, refletindo o fato de que, para a maioria dos hardwares, os exemplos são gerenciados separadamente de SRVs, UAVs, CBVs.

Os heaps de descritores desses tipos podem ser solicitados para que o sombreador seja visível ou não quando o heap é criado (o último – sem sombreador visível-pode ser útil para descritores de preparo na CPU). Quando solicitado a estar visível para sombreador, cada um dos tipos de heap acima pode ter um limite de tamanho de hardware para qualquer alocação de heap de descritor individual.

Os aplicativos podem criar qualquer número de heaps de descritores, e heaps de descritor não visíveis não são restritos em tamanho. Se um sombreador de descritor visível que é criado pelo aplicativo for menor do que o limite de tamanho de hardware, o driver poderá optar por subalocar o heap de descritor fora de um heap de descritor subjacente maior para que vários heaps de descritores de API caibam em um heap de descritor de hardware. O motivo disso pode acontecer é que, para alguns hardwares, alternar entre heaps de descritores de hardware durante a execução requer uma espera de GPU para ociosidade (para garantir que as referências de GPU para o heap descritor anteriormente sejam concluídas). Se todos os heaps de descritores que um aplicativo cria se ajustarem às capacidades máximas do heap de hardware aplicável, não ocorrerá nenhuma espera durante a alternância de heaps de descritor de API durante a renderização. No entanto, os aplicativos devem permitir a possibilidade de que alternar o heap do descritor atual possa incorrer em uma espera por ociosidade.

Para evitar ser afetado por essa possível espera por ociosidade na alternância de heap do descritor, os aplicativos podem aproveitar as interrupções na renderização que poderiam fazer com que a GPU fique ociosa por outros motivos como o tempo para fazer comutadores de heap de descritor, já que uma espera por ociosidade está ocorrendo mesmo assim.

O mecanismo e a semântica para identificar heaps de descritores para sombreadores durante a gravação da lista de comandos/pacote são descritos na referência de API.

## <a name="an-example"></a>Um exemplo

A imagem abaixo mostra dois heaps de descritores que fazem referência a duas texturas 2D separadas que estão sendo armazenadas em dois slots de um heap padrão grande. O heap do descritor que está visível para sombreador pode ser acessado pelo pipeline de gráficos (incluindo os sombreadores) e, portanto, a textura 2D está disponível para o pipeline.

![heaps de descritor visíveis e não visíveis](images/descriptor-heaps.png)

> [!Note]  
> Geralmente, há um limite de hardware de GPU da quantidade de memória local de GPU gravável pela CPU (conhecida como memória combinada de gravação) para heaps de descritores. Normalmente, esse limite está em volta de 96MB para todos os processos. Um heap de descritor de membro 1 milhão, com 32Byte descriprs, usaria 32 MB, por exemplo. O driver fará o fallback na memória do sistema, se necessário, embora seja uma prática recomendada não criar grandes números de heaps de descritor grandes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




