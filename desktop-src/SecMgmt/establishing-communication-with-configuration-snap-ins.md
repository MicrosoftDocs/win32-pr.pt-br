---
description: Depois que sua extensão de snap-in de anexo tiver sido adicionada ao nó de serviços, ela deverá estabelecer a comunicação com o snap-in de configuração de segurança.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Estabelecendo a comunicação com snap-ins de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787447"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="81529-103">Estabelecendo a comunicação com snap-ins de configuração</span><span class="sxs-lookup"><span data-stu-id="81529-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="81529-104">Depois que sua extensão de snap-in de anexo tiver sido adicionada ao nó de serviços, ela deverá estabelecer a comunicação com o snap-in de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="81529-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="81529-105">Isso é necessário porque a extensão do snap-in de anexos obtém seus dados, bem como quaisquer alterações feitas pelo usuário, do snap-in de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="81529-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="81529-106">Isso pode ser feito conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="81529-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="81529-107">**Para estabelecer a comunicação com os snap-ins de configuração de segurança**</span><span class="sxs-lookup"><span data-stu-id="81529-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="81529-108">Obtenha o nome do arquivo de configuração usando o \_ formato de área de transferência de anexos CCF SCESVC \_ , que retorna o nome do arquivo de configuração como um **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="81529-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="81529-109">Se o anexo for inserido em um nó de tipo de configuração, o anexo precisará saber qual configuração é.</span><span class="sxs-lookup"><span data-stu-id="81529-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="81529-110">(Ele comunica essas informações aos snap-ins de configuração de segurança durante a inicialização da interface.) Nesse caso, use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="81529-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="81529-111">Configure o contexto com os snap-ins de configuração de segurança. Depois que o nome da configuração for conhecido ou se o nó do serviço for um nó de análise, a extensão do snap-in do anexo deverá chamar [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para configurar o contexto, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="81529-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> <span data-ttu-id="81529-112">Quando você terminar de usar o identificador retornado por [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), feche o identificador chamando a função [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="81529-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="81529-113">Isso normalmente é feito quando o usuário fecha o console do MMC.</span><span class="sxs-lookup"><span data-stu-id="81529-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 



