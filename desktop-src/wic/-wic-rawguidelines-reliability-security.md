---
description: Confiabilidade e segurança
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Confiabilidade e segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4704b84d09698fd6fabcf2d190050063ec3b3190904aa669fa78799c5d0158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441726"
---
# <a name="reliability-and-security"></a>Confiabilidade e segurança

Como Windows codecs do WIC (componente de imagens) serão invocados de dentro do shell do Windows e do Galeria de Fotos, os autores de codec devem fazer todos os esforços para garantir um alto nível de confiabilidade e segurança em seus codecs WIC.

Escrever código confiável depende em grande parte de boas práticas de codificação, revisões de código efetivas e testes de unidade completos e teste de cenário. Além disso, as diretrizes a seguir ajudarão a garantir que o codec está em conformidade com as políticas Windows Vista relacionadas à confiabilidade.

-   Habilitar o cancelamento de E/S.

    Os autores de codec devem fornecer uma maneira para o usuário final cancelar qualquer operação de execução longa. Os codecs do WIC suportam isso implementando IWICBitmapProgressNotification. Isso permite que um aplicativo de chamada especifique uma função de retorno de chamada para o codec chamar em intervalos especificados para notificar o chamador do progresso da operação atual. Quando um aplicativo retorna ERROR CANCELLED da função de retorno de chamada, o codec deve cancelar qualquer operação em andamento e propagar o HRESULT de volta para \_ o chamador. Isso é especialmente importante para codecs RAW, pois pode levar vários segundos para decodificar uma imagem RAW de tamanho completo e os aplicativos precisam de uma maneira de anular esse processamento.

-   Certifique-se de que o código seja executado no menor escopo necessário para executar sua função.

    Os autores de codec devem garantir que o codec não consuma mais recursos do que o necessário ou tenha um escopo maior do que o necessário. O escopo de um codec no WIC é um único arquivo de imagem; o codec é criado quando um arquivo de imagem é carregado e o codec é liberado quando a imagem é fechada. Como o WIC é uma plataforma extensível baseada em componentes, os codecs do WIC terão cargas e descarregamentos sobrepostos, e inicia e para, tudo dentro do mesmo processo. Se a infraestrutura subjacente de um codec exigir operações de início e parada em um escopo maior que uma única imagem, a confiabilidade será impactada. Codecs habilitados para WIC serão usados pelo Windows Explorer, bem como outros aplicativos. Portanto, se um codec permanecer carregado durante o tempo de vida do processo, a memória não será liberada com eficiência e uma falha do codec poderá desligar o Windows Explorer e, potencialmente, exigir que o computador seja reinicializado. (Considere que o codec será invocado sempre que uma imagem for miniaturada pela primeira vez no Windows Explorer: é essencial que essa seja uma operação leve.)

-   Use ferramentas de análise de código estáticas e dinâmicas.

    -   Ferramentas de análise estática:

        PREfix – para detectar erros em tempo de compilação.

        PREfast – para analisar o código para bugs.

    -   Ferramentas de análise dinâmica:

        AppVerifier – que ajuda a tornar os aplicativos mais resilientes simulando problemas comuns de software do mundo real.

-   Verifique todas as entradas nas revisões de código.

    Todos os parâmetros para métodos exportados e todos os dados de arquivo devem ser verificados cuidadosamente quanto à validade e rejeitados robustamente se houver falhas, a fim de proteger contra estouros e estouros de buffer, estouros aritméticos e subfluxos e tipos inesperados.

-   Use técnicas de difusão de arquivo para descobrir possíveis falhas e travamentos.

    A difusão de arquivo é o processo de testar o codec com entradas permutadas aleatoriamente.

    Há duas formas de difusão de arquivo: difusão não direcionada (aleatória) e difusão direcionada. A difusão não direcionada faz uma invertida de bits aleatória para ver se a entrada aleatória pode falhar o codec. A difusão direcionada permuta a entrada com base em algum conhecimento do formato de arquivo. Por exemplo, se houver uma CRC (verificação de redundância de ciclo) no deslocamento de bytes 32, alterar os bytes sem atualizar o CRC provavelmente não fará a maior parte dos caminhos de código. Neste exemplo, um difuso direcionado deve corrigir o CRC quando os bytes são modificados.

    O conjunto de entrada de imagens para difusão de arquivo deve ser criado para que cada combinação de parâmetros compatível com o decodificador seja testada. Por exemplo, se o decodificador for compatível com arquivos pequenos e big-endian e três configurações de compactação, o conjunto de entrada da imagem deverá consistir em arquivos little-endian de cada configuração de compactação e arquivos big-endian para cada configuração de compactação. Essa abordagem produzirá um conjunto grande, mas muito robusto de imagens de entrada a serem testadas. Mesmo que nenhuma câmera produza cada uma das combinações, mas o decodificador dá suporte a essas combinações teóricos, os autores de codec devem difusão essas entradas.

    A segurança pode ser bastante aprimorada pela execução regular de testes difuso de arquivos de imagem durante o desenvolvimento de codec. Os codecs sempre devem ser capazes de detectar a corrupção do arquivo de imagem e falhar normalmente no caso de uma solicitação malformada ou de dados malformados.

-   Enfatizar o código.

    Teste o codec executando-o continuamente em vários processos simultâneos, executando todas as operações com suporte em todas as sequências possíveis, em imagens de tamanhos variados (incluindo imagens muito grandes) de cada câmera com suporte.

-   Segurança de thread.

    A partir Windows 7, o WIC exige que os CODECs RAW sejam do tipo de apartment COM "Both". Isso significa que você deve fazer o bloqueio apropriado para lidar com chamadores e chamadores entre apartments em cenários de vários threads. Objetos em um MTA (Multi Threaded Apartment) podem ser chamados simultaneamente por qualquer número de threads dentro do MTA, permitindo um melhor desempenho em sistemas de vários núcleos e em determinados cenários de servidor. Além disso, os CODECs do WIC que residem em um MTA podem chamar outros objetos que residam no MTA sem o custo de marshaling associado à chamada entre threads que residam em diferentes apartments STA. No Windows 7, todos os CODECs WIC in-box foram atualizados para dar suporte a MTAs, incluindo JPEG, TIFF, PNG, GIF, ICO e BMP. CodeCs de terceiros que não deem suporte a MTAs causarão custos significativos de desempenho em aplicativos multithread devido ao marshaling. A habilitação do suporte ao MTA requer que a sincronização adequada seja implementada no CODEC de terceiros. A implementação exata dessas técnicas de sincronização está além do escopo deste artigo. Uma referência geral para sincronizar objetos COM é fornecida abaixo.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem RAW da câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



