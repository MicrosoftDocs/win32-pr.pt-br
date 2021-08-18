---
description: As interfaces a seguir são usadas por um aplicativo para gerenciar o pacote de documentos de impressão.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimir interfaces de API do pacote de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470118"
---
# <a name="print-document-package-api-interfaces"></a>Imprimir interfaces de API do pacote de documentos

As interfaces a seguir são usadas por um aplicativo para gerenciar o pacote de documentos de impressão.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Representa o progresso do trabalho de impressão.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permite que os usuários enumerem os tipos de destino de pacote com suporte e criem um com uma ID de tipo específica. O **IPrintDocumentPackageTarget** também dá suporte ao acompanhamento do progresso da impressão do pacote e ao cancelamento.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Usado com [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para iniciar um trabalho de impressão.<br/>                                                                                                               |



 

 

