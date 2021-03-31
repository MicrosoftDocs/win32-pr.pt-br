---
title: Backup em fita
description: Um volume de fita consiste em um meio de gravação e em sua operadora física. Cada volume de fita tem uma ou mais partições. Geralmente, as partições são divididas em seções por marcas de filemarcações ou marcas. Há três tipos de marcas de File.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- Backup de backup, fita
- Backup de backup em fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005060"
---
# <a name="tape-backup"></a>Backup em fita

Um *volume de fita* consiste em um meio de gravação e em sua operadora física. A duração total da fita em um volume não está disponível para a gravação de dados. As seções curtas no início e no final da fita são reservadas para anexar a fita aos hubs na operadora. A primeira posição na fita na qual os dados podem ser registrados é chamada de *marcador de início de média*, e a última posição é chamada de *marcador de fim de média*.

Cada volume de fita tem uma ou mais partições. Uma partição é uma parte do volume, contendo seus próprios pontos inicial e final, que não se sobrepõem a nenhuma outra parte do volume. Cada partição tem três posições predefinidas. A primeira posição em uma partição na qual você pode registrar dados é chamada de *marcador de início de partição*, e o último é chamado de *marcador de fim de partição*. O *marcador de aviso antecipado* está localizado imediatamente antes do marcador de fim de partição. A posição de aviso antecipada notifica os aplicativos de fita para transferir dados armazenados em buffer para a fita antes de atingir o marcador de fim de partição.

A área entre os pontos inicial e final de uma partição normalmente é dividida em seções por *marcas de filemarcações* ou *marcas*. Marcas de gravação e marcações são elementos de registro especial que não contêm dados de usuário; Eles simplesmente dividem a partição em áreas menores para fornecer um esquema de endereço. As marcações de um e-de-marcas têm finalidades semelhantes, mas as marcas definidas fornecem um posicionamento mais rápido em unidades de fita de alta capacidade.

Normalmente, os dispositivos de fita dão suporte a marcações de e-marcas. O suporte de ambos permite que os dados de fita sejam formatados de modo que os demarcadores separam dados de diferentes volumes de disco e marcas de arquivo separem dados de arquivos individuais em um volume de disco.

Outro elemento registrado que denota locais na fita é uma *lacuna de apagamento*, uma área de fita apagada ou um padrão que o dispositivo não reconhece como uma marca ou como dados do usuário.

Há três tipos de marcas de File. Uma *marca* de gravação curta contém uma pequena lacuna de apagamento que não pode ser substituída, a menos que a operação de escrita seja executada desde o início da partição ou de uma marca de um longo e anterior. Uma *marca de caixa de caracteres longa* contém uma lacuna de apagamento longa que permite que um aplicativo Posicione a fita no início da marca de e para substituir a marca de e/ou a lacuna de apagamento. Uma *marca* de erro normal não contém uma lacuna de apagamento. Os dispositivos de fita que usam marcas de e/SS oferecem suporte a marcações de filecurtas e longas ou marcações de caracteres normais, mas não a três.

A área em uma partição entre marcas ou marcas de gravação está disponível para gravar dados. Uma unidade de dados gravada ou lida de uma fita é chamada de bloco.

Para mais informações, consulte os seguintes tópicos:

-   [Inicialização de fita](tape-initialization.md)
-   [Entrada e saída de fita](tape-input-and-output.md)
-   [Criando um aplicativo de backup](creating-a-backup-application.md)
-   [Fazendo backup e restaurando links físicos](backing-up-and-restoring-hard-links.md)

 

 




