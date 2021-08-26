---
description: 'Qualquer operação de backup que tenta copiar uma imagem completa e estável de um sistema deve lidar com as seguintes preocupações:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemas comuns de backup de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16275c0d8e9128110736dd5feb51c75d2977b77c746b56cda487eed3aec86c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032886"
---
# <a name="common-volume-backup-issues"></a>Problemas comuns de backup de volume

Qualquer operação de backup que tenta copiar uma imagem completa e estável de um sistema deve lidar com as seguintes preocupações:

-   Arquivos inacessíveis durante um backup. A execução de aplicativos frequentemente precisa manter os arquivos abertos no modo exclusivo durante um backup, impedindo que os programas de backup os copiem.
-   Estado do arquivo inconsistente. Mesmo que um aplicativo não tenha seus arquivos abertos no modo exclusivo, é possível, devido ao tempo finito necessário para abrir, fazer o back-up e fechar um arquivo, que os arquivos copiados para a mídia de armazenamento podem nem todos refletir o mesmo estado do aplicativo.
-   Precisa minimizar as interrupções de serviço. Para garantir a acessibilidade do arquivo e a integridade dos dados que estão sendo backupados pode exigir a suspensão e/ou o encerramento de todos os programas em execução durante um backup de volume. Para sistemas de disco grandes, isso pode ter horas de duração.

    Recentemente, alguns fornecedores de armazenamento tentaram resolver esses problemas fornecendo um mecanismo de captura de volume – um meio de capturar uma imagem dos arquivos no disco em um determinado instante no tempo – usando um mecanismo de cópia na gravação ou "espelho dividido". No entanto, essas soluções envolvem suas próprias dificuldades:

    -   Implementações incompatíveis de fornecedor da captura de volume. Muitos provedores de dispositivos RAID fornecem mecanismos de captura de volume. No entanto, cada fornecedor tem sua própria interface e cada um deve obter suporte dos fornecedores de backup para suas interfaces de captura de volume. Isso significa que os fornecedores de aplicativos de backup devem dar suporte a várias implementações de captura de volume, o que é indesejável.
    -   Falta de coordenação de aplicativos. Muitos dispositivos que suportam uma captura de volume não são compatíveis com a coordenação de aplicativos em execução com o congelamento de dados em disco. Para esses dispositivos que têm, assim como nos aplicativos de backup, cada fornecedor tem uma interface diferente.
    -   Suporte limitado para dispositivos não RAID. Poucos se algum fornecedor de disco convencional fornecer suporte para qualquer tipo de captura de volume em seus drivers de dispositivo. Isso significa que os mecanismos de captura são limitados a determinados sistemas de disco e normalmente não podem dar suporte ao backup de áreas do sistema.
    -   Precisa lidar com atualizações no disco durante a captura de volume. Embora os mecanismos de captura de volume fornecidos pelo fornecedor de armazenamento possam congelar o estado dos dados no disco, eles nem sempre interoperam com aplicativos em execução. Isso frequentemente significa que os dados enviados para o volume enquanto um dispositivo de armazenamento está passando pela captura de volume podem ser perdidos.
    -   Backup multivolume consistente. O dispositivo de armazenamento executa essas capturas de volume, portanto, geralmente não há nenhum mecanismo para coordenar o tempo do congelamento de dados. Isso é particularmente verdadeiro se os dispositivos vêm de fornecedores separados. Portanto, se vários volumes de armazenamento estão envolvidos em um backup com uma captura de volume, a imagem de tempo preservada para cada volume pode não ser consistente.

 

 



