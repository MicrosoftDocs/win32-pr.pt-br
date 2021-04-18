---
description: Uma extensão de snap-in de anexo é o componente de um anexo que exibe a interface do usuário específica do serviço.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Extensões de snap-in de anexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105770323"
---
# <a name="attachment-snap-in-extensions"></a><span data-ttu-id="74e2c-103">Extensões de snap-in de anexos</span><span class="sxs-lookup"><span data-stu-id="74e2c-103">Attachment Snap-in Extensions</span></span>

<span data-ttu-id="74e2c-104">Uma extensão de snap-in de anexo é o componente de um anexo que exibe a interface do usuário específica do serviço.</span><span class="sxs-lookup"><span data-stu-id="74e2c-104">An attachment snap-in extension is the component of an attachment that displays the service-specific user interface.</span></span> <span data-ttu-id="74e2c-105">A extensão do snap-in é hospedada pelos snap-ins de configuração de segurança. A comunicação entre a extensão de anexo e seu host de snap-in é tratada pelos mecanismos padrão do MMC descritos na documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="74e2c-105">The snap-in extension is hosted by the Security Configuration snap-ins. The communication between the attachment extension and its snap-in host is handled by the standard MMC mechanisms described in the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="74e2c-106">Além das interfaces para as quais a extensão de snap-in deve dar suporte para ser uma extensão de snap-in do MMC, uma extensão de snap-in de anexos também deve oferecer suporte à interface COM, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="74e2c-106">In addition to the interfaces that the snap-in extension must support in order to be an MMC snap-in extension, an attachment snap-in extension must also support the COM interface, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="74e2c-107">Essa interface implementa métodos que indicam se há dados específicos do serviço que devem ser salvos no banco de dado de segurança e, nesse caso, recuperar e salvar esses novos dados.</span><span class="sxs-lookup"><span data-stu-id="74e2c-107">This interface implements methods that indicate whether there is service-specific data that should be saved to the security database, and if so, retrieve and save this new data.</span></span> <span data-ttu-id="74e2c-108">Os snap-ins de configuração de segurança chamam métodos dessa interface regularmente para atualizar o banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="74e2c-108">The Security Configuration snap-ins call methods of this interface regularly in order to update the security database.</span></span>

<span data-ttu-id="74e2c-109">Os snap-ins de configuração de segurança implementam uma interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que fornece métodos para recuperar dados específicos do serviço do banco de dado de segurança.</span><span class="sxs-lookup"><span data-stu-id="74e2c-109">The Security Configuration snap-ins implement an interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), that provides methods to retrieve service-specific data from the security database.</span></span> <span data-ttu-id="74e2c-110">As extensões de snap-in de anexos podem chamar métodos dessa interface para recuperar dados do banco de dado de segurança.</span><span class="sxs-lookup"><span data-stu-id="74e2c-110">Attachment snap-in extensions can call methods of this interface to retrieve data from the security database.</span></span>

<span data-ttu-id="74e2c-111">Essa arquitetura é ilustrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="74e2c-111">This architecture is illustrated in the following diagram.</span></span>

![extensões de snap-in de anexos](images/model2.png)

<span data-ttu-id="74e2c-113">Ao criar uma extensão de snap-in de anexo, você deve instalá-la e registrá-la com os snap-ins de configuração de segurança. Você faz isso adicionando chaves ao registro, conforme explicado em [registrando uma extensão de snap-in de anexo](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="74e2c-113">When you create an attachment snap-in extension, you must install it and register it with the Security Configuration snap-ins. You do this by adding keys to the registry, as explained in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span> <span data-ttu-id="74e2c-114">Quando um snap-in de configuração de segurança é iniciado, ele verifica o registro e carrega todas as extensões de snap-in registradas.</span><span class="sxs-lookup"><span data-stu-id="74e2c-114">When a Security Configuration snap-in starts, it checks the registry and loads any registered snap-in extensions.</span></span> <span data-ttu-id="74e2c-115">As extensões aparecem como nós na área de segurança para cada serviço no snap-in de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="74e2c-115">The extensions appear as nodes under the security area for each service in the Security Configuration snap-in.</span></span>

> [!Note]
> <span data-ttu-id="74e2c-116">Uma extensão de snap-in de anexos só pode estender nós de serviços.</span><span class="sxs-lookup"><span data-stu-id="74e2c-116">An attachment snap-in extension can only extend Services nodes.</span></span> <span data-ttu-id="74e2c-117">O nó serviços é o snap-in do MMC que contém ferramentas para administrar serviços instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="74e2c-117">The Services node is the MMC snap-in that contains tools to administer services installed on the system.</span></span> <span data-ttu-id="74e2c-118">A extensão de snap-in de anexos declara-se como sendo subordinada a um tipo de nó de serviços específico e, em seguida, para cada ocorrência desse tipo de nó de serviços, o console do MMC adiciona automaticamente as extensões de snap-in relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74e2c-118">The attachment snap-in extension declares itself as being a subordinate to a specific Services node type, and then for each occurrence of that Services node type, the MMC console automatically adds the related snap-in extensions.</span></span>
> 
> <span data-ttu-id="74e2c-119">Cada extensão de snap-in de anexo possui um nó de painel de escopo e o painel de resultados relacionado no MMC.</span><span class="sxs-lookup"><span data-stu-id="74e2c-119">Each attachment snap-in extension owns one scope pane node and the related result pane in MMC.</span></span>

 

 

 
