---
description: Uma extensão de snap-in de anexo fornece uma interface que os usuários podem usar para alterar as definições de configuração específicas do serviço.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Criando uma extensão de snap-in de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779346"
---
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="1f351-103">Criando uma extensão de snap-in de anexo</span><span class="sxs-lookup"><span data-stu-id="1f351-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="1f351-104">Uma extensão de snap-in de anexo fornece uma interface que os usuários podem usar para alterar as definições de configuração específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="1f351-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="1f351-105">A extensão do snap-in de anexos deve atender aos requisitos do MMC para ser uma extensão de snap-in válida.</span><span class="sxs-lookup"><span data-stu-id="1f351-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="1f351-106">Para obter mais informações sobre esses requisitos, consulte a documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="1f351-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="1f351-107">Além das interfaces exigidas pelo MMC, uma extensão de snap-in de anexos deve implementar a interface COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="1f351-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="1f351-108">Os snap-ins de configuração de segurança chamam métodos dessa interface para determinar se os dados de configuração foram alterados e, nesse caso, para atualizar o banco de dado de segurança.</span><span class="sxs-lookup"><span data-stu-id="1f351-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="1f351-109">O snap-in de anexo deve armazenar quaisquer alterações de configuração até que os snap-ins de configuração de segurança recuperem esses dados.</span><span class="sxs-lookup"><span data-stu-id="1f351-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="1f351-110">Uma extensão de snap-in de anexo deve fornecer a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="1f351-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="1f351-111">Exibir informações de configuração e análise</span><span class="sxs-lookup"><span data-stu-id="1f351-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="1f351-112">Modificar as informações de configuração na interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1f351-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="1f351-113">Modificar informações de configuração no banco de dados de segurança</span><span class="sxs-lookup"><span data-stu-id="1f351-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="1f351-114">Para auxiliar sua extensão de snap-in na execução dessas tarefas, os snap-ins de configuração de segurança implementam uma interface COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que fornece métodos que sua extensão de snap-in pode chamar para se inicializar e consultar informações do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="1f351-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="1f351-115">Depois de criar sua extensão de snap-in de anexo, você deve registrá-la com os snap-ins de configuração de segurança, conforme descrito em [registrando uma extensão de snap-in de anexo](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="1f351-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 
