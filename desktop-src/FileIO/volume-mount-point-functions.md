---
description: Funções usadas para gerenciar pastas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funções de pasta montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870776"
---
# <a name="mounted-folder-functions"></a>Funções de pasta montadas

As funções de pasta montadas podem ser divididas em três grupos: funções de uso geral, funções usadas para verificar volumes e funções usadas para verificar um volume para pastas montadas.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose funções de pasta montada



| Função                                                                     | Descrição                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Exclui uma letra da unidade ou uma pasta montada.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera o caminho guid do volume para o volume associado ao ponto de montagem de volume especificado (letra da unidade, caminho do GUID do volume ou pasta montada). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera a pasta montada associada ao volume especificado.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Associa um volume a uma letra da unidade ou um diretório em outro volume.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning funções



| Função                                   | Descrição                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Retorna o nome de um volume em um computador. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) é usado para começar a enumerar os volumes de um computador. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continua uma pesquisa de volume iniciada por uma chamada para [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Fecha uma pesquisa de volumes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funções de verificação de pasta montadas



| Função                                                       | Descrição                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera o nome de uma pasta montada no volume especificado. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) é usado para iniciar a verificação das pastas montadas em um volume. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continua uma pesquisa de pasta montada iniciada por uma chamada para [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Fecha uma pesquisa de pastas montadas.                                                                                                                                                      |



 

 

 



