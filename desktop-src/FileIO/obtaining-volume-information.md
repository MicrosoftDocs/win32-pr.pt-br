---
description: Antes de acessar arquivos e diretórios em um determinado volume, você deve determinar os recursos do sistema de arquivos usando a função GetVolumeInformation.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Obtendo informações de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501986"
---
# <a name="obtaining-volume-information"></a>Obtendo informações de volume

A função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) recupera informações sobre o sistema de arquivos em um determinado volume. Essas informações incluem o nome do volume, o número de série do volume, o nome do sistema de arquivos, os sinalizadores do sistema de arquivos, o comprimento máximo de um nome de arquivo e assim por diante. Antes de acessar arquivos e diretórios em um determinado volume, você deve determinar os recursos do sistema de arquivos usando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Essa função retorna valores que você pode usar para adaptar seu aplicativo para trabalhar com eficiência com o sistema de arquivos.

Em geral, você deve evitar o uso de buffers estáticos para nomes de arquivos e caminhos. Em vez disso, use os valores retornados por [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) para alocar buffers conforme necessário. Se você precisar usar buffers estáticos, Reserve 256 caracteres para nomes de arquivo e 260 caracteres para caminhos.

As funções [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) e [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recuperam os caminhos para o diretório do sistema e o diretório do Windows, respectivamente.

A função [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) recupera informações organizacionais sobre um volume, incluindo o número de bytes por setor, o número de setores por cluster, o número de clusters livres e o número total de clusters. No entanto, **GetDiskFreeSpace** não pode relatar tamanhos de volume maiores que 2 GB. Para garantir que seu aplicativo funcione com discos rígidos de grande capacidade, use a função [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) .

A função [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) indica se o volume referenciado pela letra da unidade especificada é uma unidade removível, fixa, CD-ROM, RAM ou rede.

A função [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifica os volumes presentes. A função [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) recupera uma cadeia de caracteres terminada em nulo para cada volume presente. Use essas cadeias de caracteres sempre que um diretório raiz for necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reconhecimento do sistema de arquivos](file-system-recognition.md)
</dt> </dl>

 

 
