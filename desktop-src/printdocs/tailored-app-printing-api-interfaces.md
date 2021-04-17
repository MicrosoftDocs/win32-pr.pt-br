---
description: As interfaces a seguir são usadas por um aplicativo para gerenciar o pacote de documentos de impressão.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimir interfaces de API do pacote de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783703"
---
# <a name="print-document-package-api-interfaces"></a>Imprimir interfaces de API do pacote de documentos

As interfaces a seguir são usadas por um aplicativo para gerenciar o pacote de documentos de impressão.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Representa o progresso do trabalho de impressão.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permite que os usuários enumerem os tipos de destino de pacote com suporte e criem um com uma ID de tipo específica. O **IPrintDocumentPackageTarget** também dá suporte ao acompanhamento do progresso da impressão do pacote e ao cancelamento.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Usado com [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para iniciar um trabalho de impressão.<br/>                                                                                                               |



 

 

