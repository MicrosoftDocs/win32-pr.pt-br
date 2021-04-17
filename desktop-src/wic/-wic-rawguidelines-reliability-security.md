---
description: Confiabilidade e segurança
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Confiabilidade e segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784176"
---
# <a name="reliability-and-security"></a>Confiabilidade e segurança

Como os codecs do Windows Imaging Component (WIC) serão invocados de dentro do shell do Windows e da Galeria de fotos, os autores de codec devem fazer cada esforço para garantir um alto nível de confiabilidade e segurança em seus codecs de WIC.

Escrever código confiável depende amplamente de práticas recomendadas de codificação, revisões de código eficazes e testes de unidade e testes de cenário completos. Além disso, as diretrizes a seguir ajudarão a garantir que o codec seja compatível com as políticas do Windows Vista relativas à confiabilidade.

-   Habilitar O cancelamento de e/s.

    Os autores de codec devem fornecer uma maneira para o usuário final cancelar qualquer operação de execução longa. Os codecs do WIC dão suporte a isso implementando IWICBitmapProgressNotification. Isso permite que um aplicativo de chamada especifique uma função de retorno de chamada para o codec chamar em intervalos especificados para notificar o chamador do progresso da operação atual. Quando um aplicativo retorna um erro \_ cancelado da função de retorno de chamada, o codec deve cancelar qualquer operação em andamento e propagar o HRESULT de volta para o chamador. Isso é especialmente importante para codecs BRUTOs, pois pode levar vários segundos para decodificar uma imagem bruta de tamanho completo e os aplicativos precisam de uma maneira de anular esse processamento.

-   Certifique-se de que o código seja executado no menor escopo necessário para executar sua função.

    Os autores de codecs devem garantir que o codec não consuma mais recursos do que o necessário ou tenha um escopo maior do que o necessário. O escopo de um codec no WIC é um arquivo de imagem única; o codec é criado quando um arquivo de imagem é carregado e o codec é liberado quando a imagem é fechada. Como o WIC é uma plataforma baseada em componente extensível, os codecs do WIC terão cargas e descarregamentos sobrepostos, e serão iniciados e interrompidos no mesmo processo. Se a infraestrutura subjacente de um codec exigir operações de iniciar e parar em um escopo maior que uma única imagem, a confiabilidade será afetada. Os codecs habilitados para WIC serão usados pelo Windows Explorer, bem como por outros aplicativos. Portanto, se um codec permanecer carregado durante o tempo de vida do processo, a memória não será liberada com eficiência e uma falha do codec poderá travar o Windows Explorer e, potencialmente, exigir que o computador seja reinicializado. (Considere que o codec será invocado toda vez que uma imagem for reminiatura pela primeira vez no Windows Explorer: é essencial que essa seja uma operação leve.)

-   Use ferramentas de análise de código estáticos e dinâmicas.

    -   Ferramentas de análise estática:

        Prefixo-para detectar erros no tempo de compilação.

        PREfast – para analisar o código de bugs.

    -   Ferramentas de análise dinâmica:

        AppVerifier – que ajuda a tornar os aplicativos mais resilientes, simulando problemas comuns de software real.

-   Verifique todas as entradas nas revisões de código.

    Todos os parâmetros para métodos exportados e todos os dados de arquivo devem ser cuidadosamente verificados quanto à validade e serem rejeitados de forma robusta se houver falha, a fim de se proteger contra estouros de buffer e subexecuções, estouros e estouros aritméticos e tipos inesperados.

-   Use técnicas de difusão de arquivos para descobrir possíveis falhas e travamentos.

    A difusão de arquivos é o processo de testar o codec com entradas permutadas aleatoriamente.

    Há duas formas de difusão de arquivos: difusão não direta (aleatória) e difusão direcionada. A difusão não direcionada faz algum bit aleatório se invertendo para ver se a entrada aleatória pode travar o codec. A difusão direcionada permuta a entrada com base em algum conhecimento do formato de arquivo. Por exemplo, se houver uma CRC (verificação de redundância de ciclo) no deslocamento de byte 32, a alteração de qualquer byte sem Atualizar o CRC provavelmente não irá exercitar a maior parte do caminhos. Neste exemplo, um difusor direcionado deve corrigir o CRC quando qualquer byte for modificado.

    O conjunto de entradas de imagens para difusão de arquivos deve ser criado para que cada combinação de parâmetros que o decodificador dê suporte seja testada. Por exemplo, se o decodificador oferecer suporte a arquivos pequenos e big-endian e três configurações de compactação, o conjunto de entrada de imagem deverá consistir em arquivos little-endian de cada configuração de compactação e em arquivos big endian para cada configuração de compactação. Essa abordagem resultará em um conjunto grande, mas muito robusto de imagens de entrada a ser testada. Mesmo que nenhuma câmera produza cada uma das combinações, mas o decodificador dá suporte a essas combinações teóricas, os autores de codec devem difundir essas entradas.

    A segurança pode ser bastante aprimorada executando testes de difusão regulares de arquivos de imagem durante o desenvolvimento do codec. Os codecs sempre devem ser capazes de detectar corrupção de arquivo de imagem e falhar normalmente no caso de uma solicitação malformada ou de dados malformados.

-   Enfatize o código.

    Teste o codec executando-o continuamente em vários processos simultâneos, executando todas as operações com suporte em todas as sequências possíveis, em imagens de tamanhos variados (incluindo imagens muito grandes) de todas as câmeras com suporte.

-   Segurança do thread.

    A partir do Windows 7, o WIC exige que os CODECs BRUTOs sejam do tipo apartment COM "both". Isso significa que você deve fazer o bloqueio apropriado para lidar com chamadores entre apartamento e chamadores em cenários multi-threaded. Os objetos dentro de um MTA (multithreaded apartment) podem ser chamados simultaneamente por qualquer número de threads no MTA, permitindo um melhor desempenho em sistemas de vários núcleos e em certos cenários de servidor. Além disso, os CODECs do WIC que residem em um MTA podem chamar outros objetos que residem no MTA sem o custo de Marshalling associado à chamada entre threads que residem em apartments STA diferentes. No Windows 7, todos os CODECs de WIC na caixa foram atualizados para dar suporte a MTAs, incluindo JPEG, TIFF, PNG, GIF, ICO e BMP. os CODECs de terceiros que não oferecem suporte a MTAs causarão custos de desempenho significativos em aplicativos multithread devido ao marshaling. Habilitar o suporte ao MTA requer que a sincronização adequada seja implementada no CODEC de terceiros. A implementação exata dessas técnicas de sincronização está além do escopo deste documento. Uma referência geral para a sincronização de objetos COM é fornecida abaixo.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



