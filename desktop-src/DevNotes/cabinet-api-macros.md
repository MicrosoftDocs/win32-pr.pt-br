---
description: 'Saiba mais sobre: macros da API do gabinete'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros da API do gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525ec84e3e857c4819b1689cade2ed0f7267dffbd8a0e0da02251a03f8d4a36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668264"
---
# <a name="cabinet-api-macros"></a>Macros da API do gabinete

Esta seção detalha as macros usadas pela API do gabinete:

## <a name="fci-macros"></a>FCI macros

As macros a seguir são usadas pelo FCI:



| Macro                                              | Descrição                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Usado para alocar memória em um contexto de FCI.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Usado para fechar um arquivo.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Usado para excluir um arquivo.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Usado para notificar quando um arquivo é colocado no gabinete.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Usado para liberar a memória alocada anteriormente em um contexto de FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Usado para solicitar informações para o próximo gabinete.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Usado para abrir um arquivo e recuperar a data, a hora e os atributos do arquivo.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Usado para obter um nome de arquivo temporário.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Usado para abrir um arquivo em um contexto FCI.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Usado para ler dados de um arquivo.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Usado para mover um ponteiro de arquivo para um local especificado.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Usado para atualizar o usuário.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Usado para gravar dados em um arquivo.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Converte o tamanho do Windows em um valor de TCOMP LXZ para [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).<br/> |



 

## <a name="fdi-macros"></a>Macros FDI

As macros a seguir são usadas por FDI:



| Macro                              | Descrição                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Usado para alocar memória em um contexto FDI.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Usado para fechar um arquivo em um contexto FDI.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Usado para atualizar o aplicativo no status do decodificador.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Usado para liberar a memória alocada anteriormente em um contexto FDI.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Usado para abrir um arquivo em um contexto FDI.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Usado para ler dados de um arquivo em um contexto FDI.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Usado para mover um ponteiro de arquivo para o local especificado em um contexto FDI.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Usado para gravar dados em um arquivo em um contexto FDI.<br/>                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de gabinete](cabinet-api-reference.md)
</dt> <dt>

[Usando a API do gabinete](using-the-cabinet-api.md)
</dt> </dl>

 

 




