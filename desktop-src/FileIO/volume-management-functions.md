---
description: Funções usadas no gerenciamento de volume.
ms.assetid: dc985126-970c-49f2-877f-3759125e43b6
title: Funções de gerenciamento de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3673e73007c977992d0209bcd79ded2afd4ed555ec3a22821e5f74d90e3cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130686"
---
# <a name="volume-management-functions"></a>Funções de gerenciamento de volume

Funções usadas no gerenciamento de volume.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)<br/>                                   | Define, redefine ou exclui nomes de dispositivo MS-DOS.<br/>                                                                                                                |
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)<br/>                     | Exclui uma letra da unidade ou uma pasta montada.<br/>                                                                                                                          |
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)<br/>                                   | Recupera o nome de um volume em um computador. <br/>                                                                                                                     |
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)<br/>               | Recupera o nome de uma pasta montada no volume especificado. <br/>                                                                                                   |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)<br/>                                     | Continua uma pesquisa de volume iniciada por uma chamada para a [**função FindFirstVolume.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) <br/>                                                           |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)<br/>                 | Continua uma pesquisa de pasta montada iniciada por uma chamada para a [**função FindFirstVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) <br/>                               |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)<br/>                                   | Fecha o alça de pesquisa de volume especificado.<br/>                                                                                                                         |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)<br/>               | Fecha o alça de pesquisa de pasta montado especificado.<br/>                                                                                                                 |
| [**Getdrivetype**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)<br/>                                         | Determina se uma unidade de disco é removível, fixa, CD-ROM, disco RAM ou unidade de rede.<br/>                                                                         |
| [**Getlogicaldrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)<br/>                                 | Recupera um bitmask que representa as unidades de disco disponíveis no momento.<br/>                                                                                              |
| [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)<br/>                     | Preenche um buffer com cadeias de caracteres que especificam unidades válidas no sistema.<br/>                                                                                               |
| [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                         | Recupera informações sobre o sistema de arquivos e o volume associados ao diretório raiz especificado.<br/>                                                               |
| [**GetVolumeInformationByHandleW**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationbyhandlew)<br/>       | Recupera informações sobre o sistema de arquivos e o volume associados ao arquivo especificado.<br/>                                                                         |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)<br/> | Recupera um caminho GUID de volume para o volume associado ao ponto de montagem de volume especificado (letra da unidade, caminho **do** **GUID** do volume ou pasta montada).<br/> |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)<br/>                               | Recupera o ponto de montagem de volume em que o caminho especificado é montado.<br/>                                                                                              |
| [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)<br/>   | Recupera uma lista de letras de unidade e caminhos de pasta montados para o volume especificado.<br/>                                                                               |
| [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)<br/>                                     | Recupera informações sobre nomes de dispositivo MS-DOS.<br/>                                                                                                                   |
| [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/>                                     | Define o rótulo de um volume do sistema de arquivos.<br/>                                                                                                                            |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)<br/>                           | Associa um volume a uma letra da unidade ou um diretório em outro volume.<br/>                                                                                          |



 

As funções a seguir são usadas com pontos de montagem de volume (letras de unidade, caminhos GUID de volume e pastas montadas).

-   [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)
-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)
-   [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)
-   [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)
-   [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
-   [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)

 

 




