---
description: Métodos de codificação
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Métodos de codificação (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4366f11ea9d120d638c5600f84fc16f6c5320f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814523"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Métodos de codificação (Microsoft Media Foundation)

A maioria dos codecs de vídeo e áudio do Windows Media dá suporte a vários métodos de codificação. Saber como e quando usar cada método pode ajudá-lo a criar conteúdo compactado de alta qualidade.

Todos os métodos de codificação se concentram no buffer usado pelo decodificador para gerenciar dados de entrada compactados. Esse buffer é definido pela taxa de bits do fluxo, em bits por segundo, e pela janela de buffer, em milissegundos. Durante a codificação, o codec obedece às restrições do buffer. Para obter mais informações sobre o buffer, consulte [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codificação de taxa de bits constante

A taxa de bits para qualquer fluxo codificado por um dos codecs de áudio e vídeo do Windows Media não é constante. A codificação constante de taxa de bits (CBR) é, portanto, um termo enganoso. O recurso de distinção de um fluxo codificado em CBR é uma pequena janela de buffer, que limita a variação de tamanhos de amostra. A codificação de CBR é usada principalmente para conteúdo que é transmitido em uma rede para seu destino. Nesse cenário, é importante ser capaz de contar com o uso consistente da largura de banda.

De um ponto de vista de configuração, a codificação de CBR difere dos outros modos que antes de começar a codificar, você define a taxa média de bits do conteúdo de saída e a janela de buffer que se aplica a essa taxa de bits. Em outros modos, um ou ambos os valores são desconhecidos quando você configura o codificador e é calculado pelo codec enquanto ele codifica. A CBR é o modo de codificação padrão usado pelo Windows Media Encoder DMOs.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass a codificação da taxa de bits constante

A CBR padrão usa apenas uma única passagem de codificação. Você fornece seu conteúdo como exemplos de entrada e o codec compacta o conteúdo e retorna exemplos de saída. Também é possível processar amostras de entrada duas vezes. Na primeira passagem, o codec executa cálculos para otimizar a codificação para o seu conteúdo. Na segunda passagem, o codec usa os dados coletados durante a primeira passagem para codificar o conteúdo.

A codificação de CBR de duas passagens tem muitas vantagens. Ele geralmente gera ganhos de qualidade significativos em relação à codificação de CBR padrão sem alterar nenhum dos requisitos de buffer. Isso torna esse modo de codificação ideal para o conteúdo que é transmitido por uma rede. A única situação em que a CBR em duas passagens não é viável é quando você codifica o conteúdo de uma fonte dinâmica e não pode usar uma segunda passagem.

O tipo de mídia de saída de um fluxo de CBR de duas passagens é idêntico ao de um fluxo de CBR padrão; Você ainda especifica a taxa de bits e a janela de buffer a ser usada. Ao configurar o DMO, você deve defini-lo para executar duas passagens. E você deve notificar o DMO quando terminar de enviar amostras para a primeira passagem.

## <a name="quality-based-variable-bit-rate-encoding"></a>Codificação de taxa de bits de variável Quality-Based

Como a codificação de CBR não mantém realmente uma taxa de bits constante, a distinção entre ela e a taxa de bits variável (VBR) pode parecer um pouco de Hazy. A principal diferença entre CBR e VBR é o tamanho da janela de buffer usada. Fluxos de taxa de bits codificados geralmente têm janelas de buffer grandes em comparação com os fluxos codificados em CBR. A VBR baseada em qualidade não é exceção, pois você não define nenhuma taxa de bits nem janela de buffer para ela. Em vez disso, você define um valor de qualidade. Em seguida, o codec tenta compactar os dados para que a qualidade da mídia codificada seja consistente durante toda a duração, independentemente dos requisitos de buffer do fluxo resultante.

A VBR baseada em qualidade usa uma única passagem de codificação e tende a criar grandes fluxos compactados. Quando a codificação é concluída, o codec define os requisitos de buffer para que o decodificador possa descompactar os dados. O fluxo VBR codificado não é adequado para streaming em uma rede, portanto, a taxa de bits baseada em qualidade deve ser usada somente para cenários de reprodução local (ou download e reprodução).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codificação de taxa de bits variável irrestrita

Diferentemente da VBR baseada em qualidade, a VBR não restringida não é codificada para um nível de qualidade específico. Em vez disso, ele codifica o conteúdo para a melhor qualidade possível e, ao mesmo tempo, mantém uma taxa de bits especificada. A VBR não restringida usa duas passagens de codificação e é semelhante à CBR de duas passagens, exceto que você não especifica uma configuração de janela de buffer para o fluxo. Isso significa que não há nenhum limite para o tamanho de amostras individuais no fluxo, desde que a taxa de bits média seja menor ou igual ao valor definido.

A VBR não restrita é de uso limitado, pois há poucos cenários de reprodução que têm requisitos para manter seus requisitos de buffer. O codec pode definir a janela de buffer para qualquer valor necessário após a codificação, dando-lhe nenhum controle sobre o tamanho do buffer. Na maioria dos casos, se você não estiver preocupado com o tamanho do buffer ou a consistência do uso de largura de banda, deverá usar a taxa de bits baseada em qualidade.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Codificação de taxa de bits de variável Peak-Constrained

O modo de codificação final é uma taxa de bits de pico restrita. Como uma VBR não restringida, esse modo usa duas passagens de codificação e codifica para uma taxa de bits especificada. No entanto, com a taxa de bits restrita de pico, você também configura o valor de pico para a codificação. Os valores de pico são semelhantes aos valores de configuração de buffer normais: há uma taxa de bits de pico e uma janela de buffer de pico. O arquivo é codificado para estar em conformidade com um buffer descrito pelos valores de pico, com a condição de que a taxa de bits média geral do fluxo seja igual ou menor que o valor médio de taxa de bits especificado.

A taxa de bits restrita pode ser difícil de conceituar. Aqui está a maneira mais fácil de considerar o modelo de buffer usado. Suponha que o fluxo seja um fluxo de CBR com a janela taxa de bits de pico e buffer de pico usada para definir o buffer. Normalmente, a taxa de bits de pico é muito alta. O codificador garante que o valor da taxa de bits média esperada que você indica seja mantido durante a duração do fluxo. Em qualquer ponto específico no fluxo, a taxa média de bits é garantida como maior que o tamanho total do fluxo em bits dividido pela duração do fluxo em segundos).

Considere o exemplo a seguir: Configure um fluxo com uma taxa média de bits de 16.000 bits por segundo, uma taxa de bits de pico de 48.000 bits por segundo e uma janela de buffer de pico de 3.000 (3 segundos). O tamanho do buffer usado para o fluxo é de 144.000 bits (48.000 bits por segundo x 3 segundos) conforme determinado pelos valores de pico. O codificador compacta os dados para que estejam em conformidade com esse buffer. Além disso, a taxa média de bits do fluxo deve ser de 16.000 ou menos. Se o codificador precisar fazer alguns exemplos muito grandes para lidar com um segmento complexo de conteúdo, ele poderá aproveitar o tamanho do buffer grande. Mas outras partes do fluxo devem ser codificadas em uma taxa de bits inferior para reduzir a média para o nível especificado.

A codificação de taxa de bits de pico restrita é útil para dispositivos de reprodução com uma capacidade de buffer finita e algumas restrições de taxa de dados. Um exemplo comum disso é a codificação usada para DVDs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a codificação de VBR](usingvbrencoding.md)
</dt> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



