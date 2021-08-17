---
title: Visão geral dos heaps de descritores
description: Heaps de descritores contêm muitos tipos de objeto que não fazem parte de um PSO (objeto de estado de pipeline), como SRVs (exibições de recursos de sombreamento), UAVs (exibições de acesso não ordenado), CBVs (exibições de buffer de constantes) e amostras.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d0017f10a6027fc7ce48618a9d28bd4e92262d83d0f3aa81cc0bc8d02b7edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124331"
---
# <a name="descriptor-heaps-overview"></a>Visão geral dos heaps de descritores

Heaps de descritores contêm muitos tipos de objeto que não fazem parte de um PSO (objeto de estado de pipeline), como SRVs (exibições de recursos de sombreamento), UAVs (exibições de acesso não ordenado), CBVs (exibições de buffer de constantes) e amostras.

-   [A finalidade dos heaps de descritor](#the-purpose-of-descriptor-heaps)
-   [Sincronização](#synchronization)
-   [Associação](#binding)
-   [Alternando heaps](#switching-heaps)
-   [Pacotes](#bundles)
-   [Gerenciamento](#management)
-   [Tópicos relacionados](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>A finalidade dos heaps de descritor

A principal finalidade de um heap de descritor é abranger a quantidade de alocação de memória necessária para armazenar as especificações de descritor dos tipos de objetos que os sombreadores fazem referência para o maior número possível de uma janela de renderização (idealmente um quadro inteiro de renderização ou mais). Se um aplicativo estiver alternando as texturas que o pipeline vê rapidamente da API, precisa haver espaço na pilha do descritor para definir tabelas de descritores em tempo real para cada conjunto de estado necessário. O aplicativo pode optar por reutilizar as definições se os recursos forem usados novamente em outro objeto, por exemplo, ou apenas atribuir o espaço de heap sequencialmente, pois ele alterna vários tipos de objeto.

Os heaps de descritores também permitem que componentes de software individuais gerenciem o armazenamento do descritor separadamente um do outro.

Todos os heaps são visíveis para a CPU. O aplicativo também pode solicitar quais propriedades de acesso da CPU um heap de descritor deve ter (se houver) – gravar combinado, gravar novamente e assim por diante. Os aplicativos podem criar quantos heaps de descritor forem desejados com quaisquer propriedades desejadas. Os aplicativos sempre têm a opção de criar heaps de descritores que são puramente para fins de preparo que não são restringidos em tamanho e copiando para heaps de descritores que são usados para renderização conforme necessário.

Há algumas restrições no que pode ir no mesmo heap de descritor. As entradas CBV, UAV e SRV podem estar no mesmo heap de descritor. No entanto, as entradas de amostra não podem compartilhar um heap com entradas CBV, UAV ou SRV. Normalmente, há dois conjuntos de heaps de descritores, um para os recursos comuns e o segundo para amostras.

O uso de heaps de descritores por Direct3D 12 reflete o que a maioria dos hardwares de GPU faz, o que deve exigir que os descritores estejam em tempo real apenas em heaps de descritor ou simplesmente que menos bits de endereçamento sejam necessários se esses heaps forem usados. O Direct3D 12 exige o uso de heaps de descritores, não há nenhuma opção para colocar descritores em qualquer lugar na memória.

Os heaps de descritores só podem ser editados imediatamente pela CPU, não há nenhuma opção para editar um heap de descritor pela GPU.

## <a name="synchronization"></a>Sincronização

O conteúdo do heap do descritor pode ser alterado antes, durante e após a gravação de listas de comandos que fazem referência a ele. No entanto, os descritores não podem ser alterados enquanto uma lista de comandos enviada para execução pode fazer referência a esse local, pois isso poderia invocar uma condição de corrida.

## <a name="binding"></a>Associação

No máximo um heap combinado CBV/SRV/UAV e um heap de amostra podem ser associados a qualquer momento. Esses heaps são compartilhados entre os pipelines de computação e de gráficos (descritos em seus PSOs).

## <a name="switching-heaps"></a>Alternando heaps

É aceitável que um aplicativo alterne heaps dentro da mesma lista de comandos ou em diferentes, usando as APIs [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) e [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) . Em alguns hardwares, isso pode ser uma operação cara, exigindo uma parada de GPU para liberar todo o trabalho que depende do heap de descritor associado no momento. Como resultado, se os heaps do descritor tiverem que ser alterados, os aplicativos devem tentar fazer isso quando a carga de trabalho da GPU for relativamente clara, talvez limitando as alterações no início de uma lista de comandos.

## <a name="bundles"></a>Pacotes

Com os pacotes, só pode haver uma chamada para o método [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) , e o conjunto de heaps do descritor deve corresponder exatamente àqueles da lista de comandos que chamam o pacote. Se o pacote não alterar tabelas de descritor, ele não precisará definir os heaps de descritor.

Para obter uma lista de chamadas de API que não podem ser usadas com grupos, consulte [criando e gravando listas de comandos e pacotes](recording-command-lists-and-bundles.md).

## <a name="management"></a>Gerenciamento

Para renderizar todos os objetos em uma cena, muitos descritores serão necessários e há algumas estratégias de gerenciamento diferentes que podem ser seguidas.

A estratégia mais básica seria preencher uma área atualizada do heap de descritores com todos os requisitos para a próxima chamada de desenho. Portanto, logo antes de emitir a chamada de desenho na lista de comandos, um ponteiro de tabela de descritores seria definido como o início da tabela populada recentemente. A vantagem é que não há necessidade de registrar onde qualquer descritor específico está no heap.

A desvantagem dessa estratégia é que pode haver muita repetição de descritores no heap de descrição, especialmente quando uma cena muito semelhante está sendo renderizada e esse espaço de heap de descritor será usado rapidamente. Heaps de descritores separados para aqueles que estão sendo processados na GPU e para aqueles que estão sendo gravados pela CPU provavelmente seriam necessários para evitar conflitos. Como alternativa, um sistema de subalocação pode ser usado.

Além disso, o sistema básico pode ser mais otimizado pelo uso cuidadoso de tabelas de descritores sobrepostas de uma chamada de desenho para a próxima, para que apenas os novos descritores necessários sejam adicionados.

Uma estratégia mais eficiente do que a básica seria preencher previamente os heaps de descritores com os descritores necessários para os objetos (ou materiais) que são conhecidos como parte da cena. A ideia aqui é que só é necessário definir a tabela de descritores no momento do desenho, pois o heap do descritor é preenchido antecipadamente.

Uma variação da estratégia de pré-teste é tratar o heap do descritor como uma matriz enorme, contendo todos os descritores necessários em locais conhecidos fixos. Em seguida, a chamada de desenho precisa apenas receber um conjunto de constantes que são os índices na matriz de onde os descritores precisam ser usados.

Uma otimização adicional é garantir que as constantes raiz e os descritores de raiz contenham as que são alteradas com mais frequência, em vez de posicionar constantes no heap do descritor. Para a maioria dos hardwares, essa é uma maneira eficiente de lidar com constantes.

Na prática, um mecanismo de gráficos pode usar uma estratégia diferente em situações diferentes e combinar elementos de cada estratégia para atender aos requisitos de desenho específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




