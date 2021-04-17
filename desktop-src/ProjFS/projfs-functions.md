---
title: Funções ProjFS
description: As funções a seguir são declaradas em projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105812424"
---
# <a name="projfs-functions"></a>Funções ProjFS

As funções a seguir são declaradas em projectedfslib. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Aloca um buffer que atende aos requisitos de alinhamento de memória do dispositivo de armazenamento da instância de virtualização. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Limpa o cache de caminho negativo da instância de virtualização, se estiver ativo. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indica que o provedor concluiu o processamento de um retorno de chamada do qual tinha retornado HRESULT_FROM_WIN32 (ERROR_IO_PENDING) anteriormente. |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Permite que um provedor exclua um item que foi armazenado em cache no sistema de arquivos local. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Determina se um nome contém caracteres curinga. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Compara dois nomes de arquivo e retorna um valor que indica sua ordem de agrupamento relativa. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Determina se um nome de arquivo corresponde a um padrão de pesquisa. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Fornece informações para um arquivo ou diretório para uma enumeração. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Fornece informações para um arquivo ou diretório para uma enumeração e permite que o chamador Especifique informações estendidas. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libera um buffer alocado. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Obtém o estado do arquivo em disco para um arquivo ou diretório. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Recupera informações sobre a instância de virtualização. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Converte um diretório existente em um espaço reservado de diretório. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configura uma instância de virtualização ProjFS e a inicia, disponibilizando-a para a e/s de serviço e invocar retornos de chamada no provedor. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Interrompe uma instância de virtualização ProjFS em execução, tornando-a indisponível para a e/s de serviço ou que envolva retornos de chamada no provedor. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Permite que um provedor atualize um item que foi armazenado em cache no sistema de arquivos local. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Envia o conteúdo do arquivo para ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Envia metadados de arquivo ou diretório para ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | O envia metadados de arquivo ou diretório para ProjFS e permite que o chamador Especifique informações estendidas. |
