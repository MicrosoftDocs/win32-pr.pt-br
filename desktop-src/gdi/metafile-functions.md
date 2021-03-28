---
description: As funções a seguir são usadas com metaarquivos de formato avançado.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Funções de metarquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502410"
---
# <a name="metafile-functions"></a>Funções de metarquivo

As funções a seguir são usadas com metaarquivos de formato avançado.



| Função                                                             | Descrição                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Fecha um contexto de dispositivo de metarquivo avançado.                                                                            |
| [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Copia o conteúdo de um metarquivo de formato avançado para um arquivo especificado.                                                |
| [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Cria um contexto de dispositivo para um metarquivo de formato avançado.                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Exclui um metarquivo de formato avançado ou um identificador de metarquivo de formato avançado.                                             |
| [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Uma função de retorno de chamada definida pelo aplicativo usada com a função EnumEnhMetaFile.                                       |
| [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Enumera os registros em um metarquivo de formato avançado.                                                             |
| [**GdiComment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Copia um comentário de um buffer para um metarquivo de formato avançado especificado.                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Cria um identificador que identifica o metarquivo de formato avançado armazenado no arquivo especificado.                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Recupera o conteúdo do metarquivo de formato avançado especificado e os copia em um buffer.                        |
| [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Recupera uma descrição de texto opcional de um metarquivo de formato avançado e copia a cadeia de caracteres para o buffer especificado. |
| [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Recupera o registro que contém o cabeçalho do metarquivo de formato avançado especificado.                                 |
| [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Recupera entradas de paleta opcionais do metarquivo avançado especificado.                                               |
| [**Getmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | Não está mais disponível para uso a partir do Windows 2000. Em vez disso, use [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**GetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Converte os registros de formato avançado de um metarquivo em registros de formato do Windows.                                      |
| [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Exibe a imagem armazenada no metarquivo de formato avançado especificado.                                                 |
| [**PlayEnhMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Reproduz um registro de metarquivo avançado executando as funções da interface de dispositivo de gráficos (GDI) identificadas pelo registro. |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Cria um metarquivo de formato avançado baseado em memória a partir dos dados especificados.                                               |
| [**SetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Converte um metarquivo do formato mais antigo do Windows para o novo formato aprimorado.                                          |



 

## <a name="obsolete-functions"></a>Funções obsoletas

As funções a seguir são obsoletas. Os são fornecidos para compatibilidade com os metaarquivos de formato do Windows.

-   [**CloseMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**CopyMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**Createmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**EnumMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**EnumMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**PlayMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**PlayMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
