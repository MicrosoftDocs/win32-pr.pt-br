---
description: Os buffers de vértice, representados pela interface IDirect3DVertexBuffer9, são buffers de memória que contêm dados de vértice.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Buffers de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645802"
---
# <a name="vertex-buffers-direct3d-9"></a>Buffers de vértice (Direct3D 9)

Os buffers de vértice, representados pela interface [**IDirect3DVertexBuffer9**](/windows/desktop/api) , são buffers de memória que contêm dados de vértice. Os buffers de vértice podem conter qualquer tipo de vértice-transformado ou sem transformação, aceso ou unlit, que pode ser renderizado por meio do uso dos métodos de renderização na interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Você pode processar os vértices de um buffer de vértice para realizar operações como transformação, iluminação ou gerar sinalizadores de recorte. A transformação sempre é executada.

A flexibilidade dos buffers de vértice os torna pontos de preparo ideais para a reutilização da geometria transformada. Você pode criar um buffer de vértice único, transformar, iluminar e recordar os vértices nele, e renderizar o modelo na cena quantas vezes forem necessárias sem transformá-lo novamente, mesmo com alterações de estado de renderização intercaladas. Isso é útil ao renderizar modelos que usam várias texturas: a geometria é transformada apenas uma vez e, em seguida, partes dela podem ser renderizadas conforme necessário, intercaladas com as alterações necessárias de textura. As alterações de estado de renderização feitas após os vértices serem processados entram em vigor na próxima vez em que os vértices forem processados.

-   [Descrição](#description)
-   [Pool de memória e uso](#memory-pool-and-usage)

## <a name="description"></a>Descrição

Um buffer de vértice é descrito em termos de seus recursos: se ele só pode existir na memória do sistema, se for usado somente para operações de gravação e o tipo e o número de vértices que ele pode conter. Todas essas características são mantidas em uma [**estrutura \_ desc D3DVERTEXBUFFER**](d3dvertexbuffer-desc.md) .

O membro de formato é definido como D3DFMT \_ VERTEXDATA para indicar que este é um buffer de vértice. O tipo identifica o tipo de recurso do buffer de vértice. O membro da estrutura de uso contém sinalizadores de capacidade geral. O \_ sinalizador D3DUSAGE SOFTWAREPROCESSING indica que o buffer de vértices deve ser usado com o processamento de vértice de software. A presença do \_ sinalizador WRITEONLY D3DUSAGE em uso indica que a memória de buffer de vértice é usada somente para operações de gravação. Isso libera o driver para posicionar os dados de vértice no melhor local de memória para permitir processamento e renderização rápidos. Se o \_ sinalizador WRITEONLY D3DUSAGE não for usado, será menos provável que o driver Coloque os dados em um local ineficiente para operações de leitura. Isso sacrificaria algum processamento e velocidade de renderização. Se esse sinalizador não for especificado, supõe-se que os aplicativos executam operações de leitura e gravação nos dados dentro do buffer de vértice.

Pool especifica a classe de memória que é alocada para o buffer de vértice. O \_ sinalizador D3DPOOL SYSTEMMEM indica que o sistema criou o buffer de vértice na memória do sistema.

O membro de tamanho armazena o tamanho, em bytes, dos dados do buffer de vértice. O membro FVF contém uma combinação de [D3DFVF](d3dfvf.md) que identificam o tipo de vértices que o buffer contém.

## <a name="memory-pool-and-usage"></a>Pool de memória e uso

Você pode criar buffers de vértice com o método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) , que usa o pool (classe de memória) e parâmetros de uso. **IDirect3DDevice9:: CreateVertexBuffer** também pode ser criado com um código de FVF especificado para uso em processamento de vértice de função fixa ou como a saída de vértices de processo. Para obter detalhes, consulte [buffers de vértices FVF (Direct3D 9)](fvf-vertex-buffers.md).

O \_ sinalizador D3DUSAGE SOFTWAREPROCESSING pode ser definido quando o processamento de vértices de software ou de modo misto (D3DCREATE \_ Misto \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) está habilitado para esse dispositivo. D3DUSAGE \_ SOFTWAREPROCESSING deve ser definido para buffers a serem usados com o processamento de vértice de software no modo misto, mas não deve ser definido para o melhor desempenho possível ao usar o processamento de vértice de hardware no modo misto. ( D3DCREATE \_ VERTEXPROCESSING de hardware \_ ). No entanto, definir D3DUSAGE \_ SOFTWAREPROCESSING é a única opção quando um único buffer é usado com o processamento de vértice de hardware e software. D3DUSAGE \_ SOFTWAREPROCESSING é permitido para dispositivos mistos e de software.

É possível forçar os buffers de vértice e de índice na memória do sistema, especificando D3DPOOL \_ SYSTEMMEM, mesmo quando o processamento de vértice é feito no hardware. Essa é uma maneira de evitar grandes quantidades de memória bloqueada por página quando um driver está colocando esses buffers na memória AGP.

Esta seção apresenta os conceitos necessários para entender e usar buffers de vértice em um aplicativo Direct3D. As informações são divididas nas seções a seguir.

-   [Criando um buffer de vértice (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Acessando o conteúdo de um buffer de vértice (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Renderização de um buffer de vértice (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Buffers de vértice FVF (Direct3D 9)](fvf-vertex-buffers.md)
-   [Processamento de vértice de função fixa (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Processamento de vértice programável (Direct3D 9)](programmable-vertex-processing.md)
-   [Tipos de dispositivo e requisitos de processamento de vértice (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> <dt>

[Renderização de vértices e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Buffers de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
