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
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="ba42e-103">Imprimir interfaces de API do pacote de documentos</span><span class="sxs-lookup"><span data-stu-id="ba42e-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="ba42e-104">As interfaces a seguir são usadas por um aplicativo para gerenciar o pacote de documentos de impressão.</span><span class="sxs-lookup"><span data-stu-id="ba42e-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ba42e-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ba42e-105">In this section</span></span>



| <span data-ttu-id="ba42e-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="ba42e-106">Topic</span></span>                                                                                       | <span data-ttu-id="ba42e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba42e-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba42e-108">**IPrintDocumentPackageStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="ba42e-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="ba42e-109">Representa o progresso do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="ba42e-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="ba42e-110">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="ba42e-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="ba42e-111">Permite que os usuários enumerem os tipos de destino de pacote com suporte e criem um com uma ID de tipo específica.</span><span class="sxs-lookup"><span data-stu-id="ba42e-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="ba42e-112">O **IPrintDocumentPackageTarget** também dá suporte ao acompanhamento do progresso da impressão do pacote e ao cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ba42e-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="ba42e-113">**IPrintDocumentPackageTargetFactory**</span><span class="sxs-lookup"><span data-stu-id="ba42e-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="ba42e-114">Usado com [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para iniciar um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="ba42e-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

