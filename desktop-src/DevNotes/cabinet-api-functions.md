---
description: 'Saiba mais sobre: Funções de API de Gabinete'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funções de API de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668350"
---
# <a name="cabinet-api-functions"></a>Funções de API de gabinete

Esta seção descreve as seguintes funções de API de Gabinete:

## <a name="fci-functions"></a>Funções FCI

A biblioteca FCI (Interface de Compactação de Arquivo) fornece a capacidade de criar gabinetes (também conhecidos como "arquivos CAB"). Além disso, a biblioteca fornece compactação para reduzir o tamanho dos dados de arquivo armazenados em gabinetes.



| Função                                   | Descrição                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Adiciona um arquivo ao gabinete que está sendo inventariado no momento.<br/>                                           |
| [**FCICriar**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Cria um contexto de FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Exclui um contexto de FCI aberto, liberando qualquer memória e arquivos temporários associados ao contexto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Conclui o gabinete atual.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Força a pasta atual em construção a ser concluída imediatamente.<br/>                        |



 

## <a name="fdi-functions"></a>Funções FDI

A biblioteca FDI (Interface de Descompactação de Arquivo) fornece a capacidade de extrair arquivos de gabinetes.



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrai arquivos de gabinetes.<br/>                                                          |
| [**FDICriar**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Cria um contexto FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Exclui um contexto FDI aberto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina se um arquivo é um gabinete e, se for, retorna informações descritivas.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Trunca um arquivo de gabinete começando no número de pasta especificado.<br/>                      |



 

## <a name="deprecated-functions"></a>Funções preteridas

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extrair**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API de Gabinete](cabinet-api-reference.md)
</dt> <dt>

[Usando a API de Gabinete](using-the-cabinet-api.md)
</dt> </dl>

 

 




