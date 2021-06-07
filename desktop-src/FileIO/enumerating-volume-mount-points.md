---
description: Funções a serem usadas para enumerar pastas montadas em um volume.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Enumerando pastas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b047e4af74f33d6bc56476734f0f39c41dd14f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386655"
---
# <a name="enumerating-mounted-folders"></a>Enumerando pastas montadas

As funções a seguir são usadas para enumerar as pastas montadas em um volume NTFS especificado:

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Essas funções funcionam de maneira muito semelhante às funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Para enumerar pastas montadas em um volume, primeiro descubra se o volume dá suporte a pastas montadas. Para fazer isso, use o nome do volume retornado pelas funções [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) para chamar a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Os nomes retornados incluem uma barra invertida à direita ( \\ ) para ser compatível com a função [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) e funções relacionadas. Para obter mais informações sobre as funções usadas para verificar os volumes em um computador, consulte [enumerando volumes](enumerating-volumes.md). Quando você chamar a função **GetVolumeInformation** , se "NTFS" for retornado no parâmetro *lpFileSystemNameBuffer* , o volume será um volume NTFS. O sistema de arquivos NTFS dá suporte a pastas montadas.

Se o volume for um volume NTFS, inicie uma pesquisa para as pastas montadas chamando [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Se a pesquisa for bem-sucedida, processe os resultados de acordo com os requisitos do seu aplicativo. Em seguida, use [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) em um loop para localizar e processar as pastas montadas uma de cada vez. Quando não houver mais nenhuma pasta montada a ser enumerada, feche o identificador de pesquisa chamando [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose). Observe que a pesquisa localizará apenas as pastas montadas que estão no volume especificado.

Você não deve assumir nenhuma correlação entre a ordem das pastas montadas que são retornadas por essas funções e a ordem das pastas montadas que são retornadas por outras funções ou ferramentas.

 

 



