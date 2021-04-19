---
title: Modelos de dados abstratos
description: Cada aplicativo e cada sistema operacional tem um modelo de dados abstrato.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- modelos de dados abstratos programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811589"
---
# <a name="abstract-data-models"></a>Modelos de dados abstratos

Cada aplicativo e cada sistema operacional tem um modelo de dados abstrato. Muitos aplicativos não expõem explicitamente esse modelo de dados, mas o modelo orienta a maneira como o código do aplicativo é escrito. No modelo de programação de 32 bits (conhecido como o modelo ILP32), os tipos de dados inteiro, longo e ponteiro são 32 bits de comprimento. A maioria dos desenvolvedores usou esse modelo sem perceber. Para o histórico da API do Win32, essa é uma suposição válida (embora não necessariamente segura) a ser tomada.

No 64-bitWindows, essa suposição de paridade em tamanhos de tipo de dados é inválida. Tornar todos os tipos de dados 64 bits de comprimento desperdiçaria espaço, pois a maioria dos aplicativos não precisa do tamanho aumentado. No entanto, os aplicativos precisam de ponteiros para dados de 64 bits e precisam da capacidade de ter tipos de dados de 64 bits em casos selecionados. Essas considerações levaram à seleção de um modelo de dados abstrato chamado LLP64 (ou P64). No modelo de dados LLP64, somente os ponteiros se expandem para 64 bits; todos os outros tipos de dados básicos (inteiro e longo) permanecem 32 bits de comprimento.

Inicialmente, a maioria dos aplicativos executados no Windows de 64 bits terá sido transportada do Windows de 32 bits. É uma meta que a mesma fonte, escrita cuidadosamente, deve ser executada em ambas as janelas de 32 e 64 bits. A definição do modelo de dados não facilita essa tarefa. No entanto, garantir que o modelo de dados afete apenas os tipos de dados de ponteiro é a primeira etapa. A segunda etapa é definir um conjunto de novos tipos de dados que permitem aos desenvolvedores dimensionar automaticamente seus dados relacionados a ponteiros. Isso permite que os dados associados a ponteiros alterem o tamanho à medida que o tamanho do ponteiro muda de 32 bits para 64 bits. Os tipos de dados básicos permanecem 32 bits de comprimento, portanto, não há nenhuma alteração no tamanho dos dados no disco, nos dados compartilhados em uma rede ou nos dados compartilhados por meio de arquivos mapeados por memória. Isso alivia os desenvolvedores de grande parte do esforço envolvido na portabilidade do código de 32 bits para o Windows de 64 bits.

Esses novos tipos de dados foram adicionados aos arquivos de cabeçalho da API do Windows. Portanto, você pode começar a usar os novos tipos agora. Para obter mais informações, consulte [os novos tipos de dados](the-new-data-types.md).

 

 




