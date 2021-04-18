---
description: Lista as interfaces fornecidas pelo mecanismo de anexo.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779345"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="67710-103">Interfaces de gerenciamento de segurança</span><span class="sxs-lookup"><span data-stu-id="67710-103">Security Management Interfaces</span></span>

<span data-ttu-id="67710-104">Esta seção contém páginas de referência para os seguintes grupos de interfaces:</span><span class="sxs-lookup"><span data-stu-id="67710-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="67710-105">Interfaces do mecanismo de anexo</span><span class="sxs-lookup"><span data-stu-id="67710-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="67710-106">Interfaces do mecanismo de anexo</span><span class="sxs-lookup"><span data-stu-id="67710-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="67710-107">Interface</span><span class="sxs-lookup"><span data-stu-id="67710-107">Interface</span></span>                                                            | <span data-ttu-id="67710-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="67710-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67710-109">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="67710-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="67710-110">Recupera dados de configuração e análise sobre um serviço de segurança especificado dos snap-ins de configuração de segurança. Os snap-ins de configuração de segurança expõem essa interface, que são chamadas de extensões de snap-in de conexão para informações de análise ou configuração de consulta.</span><span class="sxs-lookup"><span data-stu-id="67710-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="67710-111">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="67710-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="67710-112">Recupera informações modificadas de configuração ou análise de um snap-in de anexo.</span><span class="sxs-lookup"><span data-stu-id="67710-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="67710-113">Os snap-ins de configuração de segurança chamam essa interface para recuperar qualquer informação modificada da extensão de snap-in de anexo.</span><span class="sxs-lookup"><span data-stu-id="67710-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="67710-114">O snap-in de configuração de segurança, em seguida, armazena esses dados adequadamente no banco de dado de segurança.</span><span class="sxs-lookup"><span data-stu-id="67710-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="67710-115">Para obter mais informações sobre as interfaces COM que devem ser implementadas por extensões de snap-in, consulte a documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="67710-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
