---
title: Heaps de descritores visíveis do sombreador
description: Heaps de descritor visíveis do sombreador são heaps de descritor que podem ser referenciados por sombreadores por meio de tabelas de descritor.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96fbbb37f3337912780e5882918c0fcbc146c41f8dc60ddf3ba5d2a35c82c1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045384"
---
# <a name="shader-visible-descriptor-heaps"></a>Heaps de descritores visíveis do sombreador

Heaps de descritor visíveis do sombreador são heaps de descritor que podem ser referenciados por sombreadores por meio de tabelas de descritor.

-   [Visão geral](#overview)
-   [Um exemplo](#an-example)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Os heaps de descritor que podem ser referenciados por sombreadores por meio de tabelas de descritor vêm em alguns tipos: um tipo de heap, D3D12 \_ SRV CBV DESCRIPTOR HEAP, pode conter Exibições de Recursos do Sombreador, Exibições de Acesso Não Organizados e Exibições de Buffer Constante, tudo \_ \_ \_ \_ intercalado. Qualquer local no heap pode ser qualquer um dos tipos listados de descritores. Outro tipo de heap, D3D12 DESCRIPTOR HEAP TYPE SAMPLER, armazena apenas exemplos, refletindo o fato de que, para a maioria dos hardwares, os samplers são gerenciados separadamente de \_ \_ \_ \_ SRVs, UAVs, CBVs.

Heaps de descritor desses tipos podem ser solicitados a serem visíveis para sombreador ou não quando o heap é criado (o último , não visível para sombreador – pode ser útil para descritores de preparação na CPU). Quando solicitado a ser visível para sombreador, cada um dos tipos de heap acima pode ter um limite de tamanho de hardware para qualquer alocação de heap de descritor individual.

Os aplicativos podem criar qualquer número de heaps de descritor e heaps de descritor visíveis não sombreador não são restritos em tamanho. Se um heap de descritor visível do sombreador criado pelo aplicativo for menor do que o limite de tamanho de hardware, o driver poderá optar por sublocar o heap do descritor de um heap de descritor subjacente maior para que vários heaps de descritor de API se ajustem a um heap de descritor de hardware. O motivo pelo qual isso pode acontecer é que, para algum hardware, alternar entre heaps de descritor de hardware durante a execução requer uma espera de GPU ociosa (para garantir que as referências de GPU ao heap de descritor anteriormente sejam concluídas). Se todos os heaps de descritor que um aplicativo cria se ajustarem às capacidades máximas do heap de hardware aplicável, essas esperas não ocorrerão ao alternar heaps de descritor de API durante a renderização. No entanto, os aplicativos devem permitir a possibilidade de que a alternação do heap do descritor atual possa incorrer em uma espera ociosa.

Para evitar ser afetado por essa possível espera ociosa na opção heap do descritor, os aplicativos podem aproveitar as quebras na renderização que fazem com que a GPU ociosa por outros motivos, como o tempo para fazer comutadores de heap do descritor, já que uma espera ociosa está acontecendo de qualquer forma.

O mecanismo e a semântica para identificar heaps de descritor para sombreadores durante a lista de comandos/gravação de pacote são descritos na referência da API.

## <a name="an-example"></a>Um exemplo

A imagem abaixo mostra dois heaps de descritor que referenciam duas texturas 2D separadas armazenadas em dois slots de um heap padrão grande. O heap do descritor visível no sombreador pode ser acessado pelo pipeline de gráficos (incluindo os sombreadores) e, portanto, a textura 2D está disponível para o pipeline.

![heaps de descritor visíveis e não visíveis](images/descriptor-heaps.png)

> [!Note]  
> Geralmente, há um limite no hardware de GPU da quantidade de memória local da GPU que pode ser escrita pela CPU (conhecida como memória combinada por gravação) para heaps de descritor. Normalmente, esse limite é de cerca de 96 MB para todos os processos. Um heap de descritor de um milhão de membros, com descritores de 32byte, usaria até 32 MB, por exemplo. O driver fará fall back na memória do sistema, se necessário, embora seja uma boa prática não criar um grande número de heaps de descritor grandes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




