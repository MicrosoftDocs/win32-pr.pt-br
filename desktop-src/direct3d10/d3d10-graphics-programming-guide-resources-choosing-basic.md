---
description: Um recurso é uma coleção de dados que são usados pelo pipeline de 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Escolhendo um recurso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be887fb94f04783b01f8873fb61812bca20faa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646516"
---
# <a name="choosing-a-resource-direct3d-10"></a>Escolhendo um recurso (Direct3D 10)

Um recurso é uma coleção de dados que são usados pelo pipeline de 3D. Criar recursos e definir seu comportamento é o primeiro passo para programar seu app. Este guia aborda tópicos básicos para escolher os recursos exigidos pelo seu app.

-   [Identificar os estágios de pipeline que precisam de recursos](#identify-pipeline-stages-that-need-resources)
-   [Identificar como cada recurso será usado](#identify-how-each-resource-will-be-used)
-   [Ligando recursos a estágios de pipeline](#binding-resources-to-pipeline-stages)
-   [Tópicos relacionados](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identificar os estágios de pipeline que precisam de recursos

A primeira etapa é escolher o [estágio do pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) (ou os estágios) que usarão um recurso. Ou seja, identificar cada estágio que fará a leitura de dados de um recurso, bem como os estágios que gravarão dados em um recurso. Conhecer os estágios de pipeline onde os recursos serão usados determina as APIs que serão chamadas para associar o recurso ao estágio.

Esta tabela lista os tipos de recursos que podem ser associados a cada estágio do pipeline. Ele inclui se o recurso pode ser associado como uma entrada ou uma saída, bem como a API de associação.



| Estágio de pipeline  | Entrada/saída | Recurso               | Tipo de recurso                           | Associar API                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Assembler de entrada | Em     | Buffer de vértice          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Assembler de entrada | Em     | Buffer de índice           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Estágios de sombreador   | Em     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources), [**GSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources), [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Estágios de sombreador   | Em     | Buffer de constantes de sombreador | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Saída de fluxo   | Saída    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Fusão de saída   | Saída    | Modo de exibição de destino de renderização     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Fusão de saída   | Saída    | Modo de exibição de estêncil/profundidade     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identificar como cada recurso será usado

Depois de escolher os estágios de pipeline que seu app usará (e, portanto, os recursos que cada estágio exigirá), a próxima etapa é determinar como cada recurso será usado, ou seja, se um recurso pode ser acessado por CPU ou GPU.

O hardware em que seu app está sendo executado terá um mínimo de pelo menos uma CPU e uma GPU. Para escolher um valor de uso, considere o tipo de processador que precisa ler ou gravar no recurso a partir das opções a seguir (consulte [**\_ uso de d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Uso de recurso | Pode ser atualizado por                    | Frequência de atualização |
|----------------|--------------------------------------|---------------------|
| Padrão        | GPU                                  | com pouca frequência        |
| Dinâmico        | CPU                                  | com frequência          |
| Staging        | GPU                                  | N/D                 |
| Imutável      | CPU (somente no momento da criação de recursos) | N/D                 |



 

O uso padrão deve ser usado para um recurso que deve ser atualizado pela CPU com pouca frequência (menor do que uma vez por quadro). Idealmente, a CPU nunca escreveria diretamente em um recurso com o uso padrão para evitar possíveis penalidades de desempenho.

O uso dinâmico deve ser usado para um recurso que a CPU atualiza relativamente com frequência (uma vez ou mais por quadro). Um cenário típico para um recurso dinâmico seria criar buffers de índice e vértice dinâmico que podem ser preenchidos em tempo de execução com dados sobre a geometria visível do ponto de vista do usuário para cada quadro. Esses buffers seriam usados para renderizar somente a geometria visível ao usuário para esse quadro.

O uso de preparo deve ser usado para copiar dados de e para outros recursos. Um cenário típico seria copiar dados em um recurso com o uso padrão (que a CPU não consegue acessar) para um recurso com o uso de preparo (que pode acessar a CPU).

Recursos imutáveis devem ser usados quando os dados no recurso não forem sofrer alteração.

Outra maneira de observar a mesma ideia é pensar o que um app faz com um recurso.



| Como o app usa o recurso     | Uso de recurso       |
|---------------------------------------|----------------------|
| Carregar uma vez e nunca atualizar            | Imutável ou padrão |
| Aplicativo preenche recurso repetidamente | Dinâmico              |
| Renderizar a textura                     | Padrão              |
| Acesso da CPU aos dados da GPU                | Staging              |



 

Se você não tiver certeza de quais usos escolher, comece pelo uso do padrão, pois ele deve ser o caso mais comum. Um buffer constante de sombreador é um tipo de recurso que sempre deve ter o uso padrão.

## <a name="binding-resources-to-pipeline-stages"></a>Ligando recursos a estágios de pipeline

Um recurso pode ser associado a mais de um estágio de pipeline ao mesmo tempo, desde que as restrições especificadas quando o recurso foi criado ([**sinalizadores de uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), sinalizadores de [**Associação**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag), [**sinalizadores de acesso da CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)) sejam atendidos. Mais especificamente, um recurso pode ser vinculado como uma entrada e uma saída simultaneamente, contanto que a parte de leitura e gravação do recurso não possa ocorrer ao mesmo tempo.

Ao vincular um recurso, pense em como a GPU e a CPU terrão acesso ao recurso. Os recursos projetados para uma única finalidade (não use vários sinalizadores de uso, associação, e de acesso de cpu) terão maior chance de resultar em melhor desempenho.

Por exemplo, considere o caso de um destino de renderização usado como uma textura várias vezes. Ele pode ser mais rápido com dois recursos: um destino de renderização e uma textura usada como um recurso do sombreador. Cada recurso usaria apenas um sinalizador de ligação ([**d3d10 \_ BIND \_ process \_ target**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) ou **d3d10 \_ BIND \_ Shader \_ Resource**). Os dados seriam copiados da textura do destino de renderização para a textura do sombreador usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Isso pode melhorar o desempenho, isolando a gravação de destino de renderização da leitura do sombreador-textura. É claro que a única maneira de ter certeza é implementar as duas abordagens e medir a diferença de desempenho em seu aplicativo específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



