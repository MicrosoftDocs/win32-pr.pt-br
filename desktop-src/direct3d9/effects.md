---
description: Um efeito do Microsoft DirectX permite a integração de vértices e sombreadores de pixel com o estado do pipeline para renderizar objetos. Os efeitos são a próxima etapa lógica na combinação de sombreadores para produzir condições de renderização exclusivas.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Efeitos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ed52a3a75f4b0682be4447f02ed305cf026af6aa30a59e921f4fa23f0e2211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985977"
---
# <a name="effects-direct3d-9"></a>Efeitos (Direct3D 9)

Um efeito do Microsoft DirectX permite a integração de vértices e sombreadores de pixel com o estado do pipeline para renderizar objetos. Os efeitos são a próxima etapa lógica na combinação de sombreadores para produzir condições de renderização exclusivas.

Os efeitos também fornecem uma maneira conveniente de escrever sombreadores para diferentes versões de hardware. Como placas de vídeo diferentes dão suporte a funcionalidades diferentes, um aplicativo pode escrever várias técnicas que serão executadas em uma variedade de dispositivos. Dessa forma, se o aplicativo estiver em execução no hardware mais recente e mais alto, o aplicativo poderá executar a técnica de efeito mais sofisticada. Por outro lado, técnicas de efeito menos sofisticadas podem ser escolhidas automaticamente para serem executadas em hardware menos barato ou menos compatível.

Um efeito pode substituir o processamento de vértice e parte do processamento de pixel executado pelo pipeline de gráficos. Um exemplo de um efeito que usa um sombreador de vértice e um sombreador de pixel está no exemplo de BasicHLSL. Você pode obter esse exemplo e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

Para obter mais informações sobre efeitos, consulte estes tópicos:

-   [Escrevendo um efeito](writing-an-effect.md)
-   [Usando um efeito](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Efeitos e o pipeline 3D

O diagrama a seguir mostra o pipeline.

![diagrama do pipeline 3D](images/effects-block-diagram.png)

O pipeline transforma os dados de entrada em pixels de saída que preenchem o buffer de quadros. Os dados de entrada vêm de objetos que são compostos de vértices em espaço de objeto ou superfícies de ordem superior criadas a partir de N-patches, patches de retângulo e patches de triângulo. Depois que os dados de entrada tiverem sido mosaicodos, o pipeline executará processamento de vértice, processamento primitivo e processamento de pixel antes de gerar as cores de pixel final.

O processamento de vértices e de pixel pode ser executado pelo pipeline de função fixa ou pode ser implementado com sombreadores programáveis. O mosaico de dados de entrada, o processamento primitivo e as saídas de dados são controlados pelo estado do pipeline. Tudo isso pode ser integrado em um efeito. Um efeito define o estado que controla como o pipeline funciona. Os efeitos gerenciam sombreadores programáveis, bem como estado de função fixa.

Os efeitos podem salvar e restaurar o estado, deixando o dispositivo no mesmo estado que antes do efeito ser executado. Os tipos de estado que um efeito pode gerenciar incluem:

-   Estado do sombreador. Isso inclui criar e excluir sombreadores, definir constantes de sombreador, definir o estado do sombreador e renderizar com sombreadores.
-   Estado de textura e amostra. Isso inclui a especificação de arquivos de textura, a inicialização de estágios de textura, a criação de objetos de amostra e a configuração do estado de amostra.
-   Outro Estado de pipeline. Isso inclui Estados para a configuração de transformações, iluminação, materiais e opções de renderização. Elas podem ser variáveis globais ou locais. As variáveis podem ser definidas pelo próprio efeito ou pelo aplicativo.

Os efeitos contêm várias opções de renderização chamadas técnicas. Cada técnica encapsula variáveis globais, estado de pipeline, textura e estado de amostra e o estado do sombreador. Um único estilo é implementado em uma passagem de renderização. Uma ou mais passagens podem ser encapsuladas em uma técnica. Todas as etapas e técnicas podem ser validadas para ver se o código de efeito será executado no dispositivo de hardware.

## <a name="effects-save-and-restore-state"></a>Estado de salvamento e restauração de efeitos

Estado do gerenciamento de efeitos. O estado da palavra é usado muito amplamente aqui, pois inclui todos os tipos de informações que o pipeline precisa para especificar as condições de renderização. Isso inclui quase todas as áreas funcionais do pipeline.

As opções de renderização são controladas por técnicas e passagens. Um aplicativo renderiza um efeito definindo uma técnica ativa e Renderizando uma ou mais passagens. Toda a renderização em um efeito é feita dentro de um par correspondente de chamadas [**begin**](id3dxeffect--begin.md) e [**end**](id3dxeffect--end.md) . Quando **begin** é chamado, um stateblock é criado e o estado do dispositivo é salvo (a menos que você especifique o contrário). Depois que uma técnica renderiza as passagens que o aplicativo especifica para renderizar, **end** é chamado para encerrar a técnica ativa. O sistema de efeitos responde restaurando automaticamente o estado do pipeline que foi capturado no bloco de estado (a menos que você opte por desabilitar essa funcionalidade de salvar e restaurar).

Ao programar sequências de renderização de várias passagens, cada uma delas requer sua própria configuração de estado, os efeitos podem reduzir a manutenção necessária para controlar as alterações de estado. Para ver mais informações sobre os Estados que podem ser salvos e restaurados por efeitos, consulte [Estados de efeito (Direct3D 9)](effect-states.md).

## <a name="effects-can-share-parameters"></a>Os efeitos podem compartilhar parâmetros

Os parâmetros de efeito são todas as variáveis não estáticas declaradas em um efeito. Isso pode incluir variáveis e anotações globais. Os parâmetros de efeito podem ser compartilhados entre diferentes efeitos declarando parâmetros com a palavra-chave Shared e, em seguida, criando o efeito com um pool de efeitos.

Os efeitos clonados usam o mesmo pool de efeitos que o efeito do qual são clonados. A clonagem de um efeito faz uma cópia exata de um efeito, incluindo variáveis globais, técnicas, passagens e anotações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
