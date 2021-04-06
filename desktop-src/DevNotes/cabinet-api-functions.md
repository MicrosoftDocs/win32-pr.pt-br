---
description: 'Saiba mais sobre: funções de API de gabinete'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funções de API de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826285"
---
# <a name="cabinet-api-functions"></a>Funções de API de gabinete

Esta seção descreve as seguintes funções de API de gabinete:

## <a name="fci-functions"></a>Funções FCI

A biblioteca FCI (File Compression interface) fornece a capacidade de criar gabinetes (também conhecidos como "arquivos CAB"). Além disso, a biblioteca fornece compactação para reduzir o tamanho dos dados de arquivo armazenados em gabinetes.



| Função                                   | Descrição                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Adiciona um arquivo ao gabinete que está sendo construído no momento.<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Cria um contexto de FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Exclui um contexto Open FCI, liberando qualquer memória e arquivos temporários associados ao contexto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Conclui o gabinete atual.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Força a pasta atual em construção a ser concluída imediatamente.<br/>                        |



 

## <a name="fdi-functions"></a>Funções FDI

A biblioteca FDI (File descompression interface) fornece a capacidade de extrair arquivos de gabinetes.



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrai arquivos de gabinetes.<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Cria um contexto FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Exclui um contexto FDI aberto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina se um arquivo é um gabinete e, se for, retorna informações descritivas.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Trunca um arquivo de gabinete que começa no número de pasta especificado.<br/>                      |



 

## <a name="deprecated-functions"></a>Funções preteridas

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extração**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de gabinete](cabinet-api-reference.md)
</dt> <dt>

[Usando a API do gabinete](using-the-cabinet-api.md)
</dt> </dl>

 

 




