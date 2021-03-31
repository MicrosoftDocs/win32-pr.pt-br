---
title: Exclusão mútua
description: Exclusão mútua
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- SDK do Windows Media Format, exclusão mútua
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- SDK do Windows Media Format, exclusão mútua do MBR
- ASF (Advanced Systems Format), exclusão mútua de MBR
- ASF (formato de sistemas avançados), exclusão mútua de MBR
- SDK do Windows Media Format, taxa de bits múltipla (MBR)
- ASF (Advanced Systems Format), taxa de bits múltipla (MBR)
- ASF (formato de sistemas avançados), taxa de bits múltipla (MBR)
- exclusão mútua, sobre
- taxa de bits múltipla (MBR), exclusão mútua
- MBR (taxa de bits múltipla), exclusão mútua
- exclusão mútua, taxa de bits
- exclusão mútua, linguagem
- exclusão mútua, apresentação
- exclusão mútua, desconhecida
- exclusão mútua, recursos
- exclusão mútua, recursos avançados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823004"
---
# <a name="mutual-exclusion"></a>Exclusão mútua

Cada arquivo ASF contém um ou mais fluxos, cada um contendo dados de mídia digital. Em circunstâncias normais, cada fluxo é associado a uma única saída. Na reprodução, o objeto leitor fornece amostras para cada saída. Portanto, como padrão, cada fluxo em um arquivo ASF é entregue pelo leitor na reprodução.

Há situações em que você não deseja que todos os fluxos sejam entregues ao cliente. Por exemplo, se você criar um arquivo de vídeo com cinco fluxos de áudio, um para cada um dos cinco idiomas, você deseja que apenas um deles seja entregue por vez. A exclusão mútua é um recurso do SDK do Windows Media Format que permite especificar um número de fluxos mutuamente exclusivos que todos correspondem à mesma saída.

A exclusão mútua é definida no perfil usado para criar um arquivo. Você configura a exclusão mútua em um perfil usando objetos de exclusão mútua. Você adiciona fluxos um de cada vez ao objeto de exclusão mútua, define o tipo e inclui o objeto no perfil.

O Windows Media Format SDK reconhece quatro tipos de exclusão mútua:

-   Taxa de bits
-   Idioma
-   Apresentação
-   Unknown

## <a name="mutual-exclusion-by-bit-rate"></a>Exclusão mútua por taxa de bits

A exclusão mútua da taxa de bits é um tipo especial de exclusão mútua e é mais comumente conhecida como exclusão mútua de taxa de bits múltipla (MBR). Uma exclusão mútua de MBR contém um número de fluxos que se originam da mesma entrada, mas são codificados em taxas de bits diferentes. Ao reproduzir um arquivo com MBR, o leitor determina o melhor fluxo a ser usado com base na largura de banda disponível.

O SDK do Windows Media Format dá suporte a MBR para fluxos de áudio e vídeo. O SDK também dá suporte a um tipo especial de vídeo MBR chamado vários MBR de tamanho de vídeo. Isso é semelhante ao vídeo MBR normal, exceto pelo fato de que os fluxos individuais podem ter diferentes tamanhos de quadro. Por exemplo, você pode ter alguns fluxos no tamanho de vídeo padrão 320 x 240 e outros com taxas de bits mais altas e tamanho de vídeo 640 x 480.

## <a name="mutual-exclusion-by-language"></a>Exclusão mútua por idioma

A exclusão mútua baseada em linguagem é projetada para uso com conteúdo (geralmente áudio) registrado em várias linguagens. Uma exclusão mútua baseada em linguagem inclui vários fluxos originados de entradas exclusivas. Cada entrada tem o mesmo conteúdo, mas em um idioma diferente.

Para que a exclusão mútua por idioma funcione, o aplicativo de leitura deve incluir a lógica para selecionar o idioma apropriado. Se você escrever um aplicativo para reproduzir arquivos ASF e desejar dar suporte a arquivos com a exclusão mútua baseada em idioma, deverá selecionar o fluxo apropriado antes de começar a reprodução.

## <a name="mutual-exclusion-by-presentation"></a>Exclusão mútua por apresentação

A exclusão mútua baseada em apresentação é fornecida para dar suporte a fluxos de vídeo que contêm o mesmo conteúdo codificado com taxas de proporção diferentes. Normalmente, isso é usado ao fornecer vídeo em uma versão Letterbox (taxa de proporção 16:9), bem como formatado para telas de televisão (taxa de proporção 4:3).

A seleção de uma apresentação para reprodução é geralmente determinada pelo usuário. Se você escrever um aplicativo para reproduzir arquivos ASF e desejar dar suporte a arquivos com a exclusão mútua baseada em apresentação, deverá apresentar ao usuário a opção de selecionar um tipo de apresentação para exibição.

## <a name="unknown-mutual-exclusion"></a>Exclusão mútua desconhecida

Você pode criar uma exclusão mútua com base em qualquer critério que desejar. Todos os tipos de exclusão mútua personalizada devem ser criados usando o tipo desconhecido.

## <a name="advanced-mutual-exclusion-features"></a>Recursos avançados de exclusão mútua

Você também pode usar a exclusão mútua para atribuir fluxos a grupos que são mutuamente exclusivos uns dos outros. Por exemplo, talvez você queira ter fluxos de áudio em vários idiomas e atribuir um fluxo de vídeo diferente a cada um. Você usa a exclusão mútua para agrupar cada fluxo de áudio com seu fluxo de vídeo correspondente e tornar todos os grupos mutuamente exclusivos.

O leitor seleciona automaticamente fluxos para todas as exclusões mútuas. Para todos os tipos de exclusão mútua, exceto MBR e exclusão mútua baseada em linguagem, o leitor sempre seleciona o fluxo padrão, que é o primeiro fluxo adicionado ao objeto de exclusão mútua no perfil. Para MBR, o leitor seleciona o fluxo que melhor se adapta à largura de banda disponível no momento da reprodução. Se você não quiser usar o fluxo padrão, poderá definir a seleção de fluxo como manual antes de começar a ler um arquivo.

A seleção de fluxo manual aplica-se a todo o arquivo. Podem surgir dificuldades quando você tem exclusões mútuas de tipos diferentes no mesmo arquivo. Por exemplo, um arquivo pode conter a exclusão mútua baseada em taxa de bits e a exclusão mútua personalizada. Para selecionar um fluxo diferente do padrão na exclusão mútua personalizada, você deve usar a seleção de fluxo manual. No entanto, se você usar a seleção de fluxo manual, o leitor não selecionará automaticamente o fluxo de taxa de bits múltiplas. Você deve planejar essa eventualidade em seu aplicativo se planeja dar suporte a vários tipos de exclusão mútua em um único arquivo. Normalmente, isso significa criar suas próprias rotinas de seleção de fluxo para tipos automáticos de exclusão mútua normalmente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Usando a exclusão mútua**](using-mutual-exclusion.md)
</dt> </dl>

 

 




