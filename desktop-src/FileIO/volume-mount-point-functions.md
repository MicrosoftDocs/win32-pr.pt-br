---
description: Funções usadas para gerenciar pastas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funções de pasta montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296865"
---
# <a name="mounted-folder-functions"></a>Funções de pasta montadas

As funções de pasta montadas podem ser divididas em três grupos: funções de finalidade geral, funções usadas para examinar volumes e funções usadas para examinar um volume para pastas montadas.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose funções de pasta montadas



| Função                                                                     | Descrição                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Exclui uma letra da unidade ou uma pasta montada.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera o caminho do volume GUID do volume que está associado ao ponto de montagem do volume especificado (letra da unidade, caminho do GUID do volume ou pasta montada). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera a pasta montada que está associada ao volume especificado.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Associa um volume com uma letra de unidade ou um diretório em outro volume.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Funções de Volume-Scanning



| Função                                   | Descrição                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Retorna o nome de um volume em um computador. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) é usado para começar a enumerar os volumes de um computador. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continua uma pesquisa de volume iniciada por uma chamada para [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Fecha uma pesquisa de volumes.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funções de verificação de pasta montadas



| Função                                                       | Descrição                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera o nome de uma pasta montada no volume especificado. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) é usado para começar a verificar as pastas montadas em um volume. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continua uma pesquisa de pasta montada iniciada por uma chamada para [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Fecha uma pesquisa de pastas montadas.                                                                                                                                                      |



 

 

 



