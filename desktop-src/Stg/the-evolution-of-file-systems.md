---
title: A evolução dos sistemas de arquivos
description: Antes que os computadores tenham sido desenvolvidos para funcionar em sistemas operacionais de disco, cada computador foi criado para executar um único aplicativo proprietário, que tinha controle completo e exclusivo de todo o computador.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769175"
---
# <a name="the-evolution-of-file-systems"></a>A evolução dos sistemas de arquivos

Antes que os computadores tenham sido desenvolvidos para funcionar em sistemas operacionais de disco, cada computador foi criado para executar um único aplicativo proprietário, que tinha controle completo e exclusivo de todo o computador. O aplicativo gravaria seus dados persistentes diretamente em um disco, ou tambor, enviando comandos diretamente para o controlador de disco. O aplicativo foi responsável por gerenciar os locais absolutos dos dados no disco, garantindo que ele não estava substituindo os dados já existentes. Como apenas um aplicativo estava em execução no computador a qualquer momento, essa tarefa não era muito difícil.

O advento dos sistemas de computador que podiam executar mais de um aplicativo exigia um mecanismo para garantir que os aplicativos não gravassem os dados uns dos outros. Os desenvolvedores de aplicativos resolveram esse problema adotando um único padrão para diferenciar os setores de disco em uso daqueles que estavam livres, marcando-os adequadamente. No tempo, esses padrões são Unidos para se tornar um sistema operacional de disco, que forneceu vários serviços para os aplicativos, incluindo um sistema de arquivos para gerenciar o armazenamento persistente. Com o advento de um sistema de arquivos, os aplicativos não tinham mais que lidar diretamente com o meio de armazenamento físico. Em vez disso, eles simplesmente disseram ao sistema de arquivos para gravar blocos de dados no disco e deixar que o sistema de arquivos se preocupe com a maneira de fazer isso. Além disso, o sistema de arquivos permitia que os aplicativos criassem hierarquias de dados por meio de uma abstração conhecida como um diretório. Um diretório pode conter não apenas arquivos, mas outros diretórios que, por sua vez, podem conter seus próprios arquivos e diretórios, e assim por diante.

O sistema de arquivos forneceu um único nível de indireção entre aplicativos e o disco, e o resultado era que cada aplicativo viu um arquivo como um único fluxo contíguo de bytes no disco, embora o sistema de arquivos estivesse realmente armazenando o arquivo em setores descontínuos. O indireção liberou os aplicativos de ter que controlar a posição absoluta dos dados em um dispositivo de armazenamento.

Atualmente, praticamente todas as APIs de sistema para entrada e saída de arquivo fornecem aplicativos para gravar informações em um arquivo simples. Os aplicativos veem esse arquivo como um único fluxo de bytes que pode crescer tão grande quanto necessário até que o disco esteja cheio. Por muito tempo, essas APIs têm sido suficientes para que os aplicativos armazenem suas informações persistentes. Os aplicativos fizeram inovações significativas em como lidam com um único fluxo de informações para fornecer recursos como gravações incrementais "rápidas".

No entanto, em um mundo de objetos de componente, o armazenamento de dados em um único arquivo simples não é mais eficiente. Assim como os sistemas de arquivos surgiu da necessidade de vários aplicativos compartilharem o mesmo meio de armazenamento, por isso, agora, os objetos de componente exigem um sistema que permite que eles compartilhem armazenamento dentro da estrutura conceitual de um único arquivo. Embora seja possível armazenar os objetos separados usando o armazenamento de arquivo simples convencional, se um dos objetos aumentar de tamanho, ou se você simplesmente adicionar outro objeto, será necessário carregar o arquivo inteiro na memória, inserir o novo objeto e, em seguida, salvar o arquivo inteiro. Esse processo pode ser extremamente demorado.

A solução fornecida pelo COM é implementar um segundo nível de indireção: um sistema de arquivos em um arquivo. O armazenamento de arquivos simples requer que uma sequência contígua grande de bytes no disco seja manipulada por meio de um único identificador de arquivo com um único ponteiro de busca. Por outro lado, o armazenamento estruturado COM define como tratar uma única entidade do sistema de arquivos como uma coleção estruturada de dois tipos de objetos — armazenamentos e fluxos — que atuam como diretórios e arquivos.

 

 




