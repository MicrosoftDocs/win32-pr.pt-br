---
description: Sua extensão de snap-in deve exibir as informações atuais de configuração e análise para os usuários.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Exibindo informações de configuração e análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784134"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="aba25-103">Exibindo informações de configuração e análise</span><span class="sxs-lookup"><span data-stu-id="aba25-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="aba25-104">Sua extensão de snap-in deve exibir as informações atuais de configuração e análise para os usuários.</span><span class="sxs-lookup"><span data-stu-id="aba25-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="aba25-105">Para exibir informações, o nó de extensão de snap-in de anexos deve estender os snap-ins de configuração de segurança usando o nó serviços.</span><span class="sxs-lookup"><span data-stu-id="aba25-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="aba25-106">O nó serviços é o snap-in do MMC que administra os serviços instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="aba25-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="aba25-107">Os tipos de nó que podem ser estendidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="aba25-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="aba25-108">NodeType dos serviços de configuração = {24a7f717-1f0c-11D1-affb-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="aba25-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="aba25-109">Nó de serviços de inspeção = {678050c7-1ff8-11D1-affb-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="aba25-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="aba25-110">Quando o nó serviços é expandido, o MMC notifica todas as extensões de snap-in registradas.</span><span class="sxs-lookup"><span data-stu-id="aba25-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="aba25-111">Cada snap-in de anexo deve se inserir no nó serviços e executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="aba25-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="aba25-112">Chame **QueryInterface** para obter um ponteiro para a interface [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) exposta pelos snap-ins de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="aba25-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="aba25-113">Chame [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para informar os snap-ins de configuração de segurança que a extensão do snap-in está carregada e para estabelecer um contexto para comunicações.</span><span class="sxs-lookup"><span data-stu-id="aba25-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="aba25-114">Chame [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) para recuperar as informações de configuração do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aba25-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="aba25-115">Essa etapa pode ser executada quando a extensão do snap-in é inicializada ou quando o usuário abre seu nó.</span><span class="sxs-lookup"><span data-stu-id="aba25-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="aba25-116">Para obter mais informações, consulte [adicionando um nó de extensão de snap-in de anexo](adding-an-attachment-snap-in-extension-node.md).</span><span class="sxs-lookup"><span data-stu-id="aba25-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



