---
description: 'Qualquer operação de backup que tenta copiar uma imagem completa e estável de um sistema deve lidar com as seguintes preocupações:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemas comuns de backup de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751605"
---
# <a name="common-volume-backup-issues"></a>Problemas comuns de backup de volume

Qualquer operação de backup que tenta copiar uma imagem completa e estável de um sistema deve lidar com as seguintes preocupações:

-   Arquivos inacessíveis durante um backup. A execução de aplicativos frequentemente precisa manter os arquivos abertos em modo exclusivo durante um backup, impedindo que os programas de backup os copiem.
-   Estado de arquivo inconsistente. Mesmo que um aplicativo não tenha seus arquivos abertos no modo exclusivo, é possível — devido ao tempo finito necessário para abrir, fazer backup e fechar um arquivo — os arquivos copiados para mídia de armazenamento podem não refletir o mesmo estado do aplicativo.
-   É necessário minimizar as interrupções de serviço. Para garantir a acessibilidade do arquivo e a integridade dos dados cujo backup está sendo feito pode exigir a suspensão e/ou a rescisão de todos os programas em execução durante um backup de volume. Para sistemas de discos grandes, isso pode ser de horas de duração.

    Recentemente, alguns fornecedores de armazenamento tentaram solucionar esses problemas fornecendo um mecanismo de captura de volume – um meio de capturar uma imagem dos arquivos em disco em um determinado instante — usando um mecanismo de cópia de gravação ou de "espelho dividido". No entanto, essas soluções envolvem suas próprias dificuldades:

    -   Implementações de fornecedor incompatíveis da captura de volume. Muitos provedores de dispositivos RAID fornecem mecanismos de captura de volume. No entanto, cada fornecedor tem sua própria interface e cada uma deve ter suporte dos fornecedores de backup para suas interfaces de captura de volume. Isso significa que os fornecedores de aplicativos de backup devem dar suporte a várias implementações de captura de volume, o que é indesejável.
    -   Falta de coordenação de aplicativos. Muitos dispositivos que dão suporte a uma captura de volume não dão suporte à coordenação de aplicativos em execução com o congelamento de dados em disco. Para os dispositivos que fazem, assim como acontece com os aplicativos de backup, cada fornecedor tem uma interface diferente.
    -   Suporte limitado para dispositivos não RAID. Alguns se algum fornecedor de disco convencional fornecer suporte para qualquer tipo de captura de volume em seus drivers de dispositivo. Isso significa que os mecanismos de captura são limitados a determinados sistemas de disco e normalmente não podem dar suporte ao backup de áreas do sistema.
    -   É necessário tratar as atualizações no disco durante a captura de volume. Embora os mecanismos de captura de volume fornecidos pelo fornecedor de armazenamento possam congelar o estado dos dados em disco, eles nem sempre interoperam com aplicativos em execução. Isso geralmente significa que os dados enviados para o volume enquanto um dispositivo de armazenamento está passando por captura de volume podem ser perdidos.
    -   Backup de multivolume consistente. O dispositivo de armazenamento executa essas capturas de volume, portanto, geralmente não há nenhum mecanismo para coordenar o tempo do congelamento de dados. Isso será particularmente verdadeiro se os dispositivos vierem de fornecedores separados. Portanto, se vários volumes de armazenamento estiverem envolvidos em um backup com uma captura de volume, a imagem de tempo preservada para cada volume poderá não ser consistente.

 

 



