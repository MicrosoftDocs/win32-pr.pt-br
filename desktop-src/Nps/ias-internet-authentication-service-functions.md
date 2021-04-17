---
title: Funções de extensões do NPS
description: Funções de extensões do NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813130"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="97344-103">Funções de extensões do NPS</span><span class="sxs-lookup"><span data-stu-id="97344-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="97344-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="97344-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="97344-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="97344-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="97344-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="97344-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="97344-107">Definido pelo aplicativo</span><span class="sxs-lookup"><span data-stu-id="97344-107">Application Defined</span></span>

<span data-ttu-id="97344-108">A arquitetura para DLLs de extensão do NPS dá suporte às seguintes funções exportadas:</span><span class="sxs-lookup"><span data-stu-id="97344-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="97344-109">**RadiusExtensionFreeAttributes**</span><span class="sxs-lookup"><span data-stu-id="97344-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="97344-110">**RadiusExtensionInit**</span><span class="sxs-lookup"><span data-stu-id="97344-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="97344-111">**RadiusExtensionProcess**</span><span class="sxs-lookup"><span data-stu-id="97344-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="97344-112">**RadiusExtensionProcessEx**</span><span class="sxs-lookup"><span data-stu-id="97344-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="97344-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="97344-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="97344-114">**RadiusExtensionTerm**</span><span class="sxs-lookup"><span data-stu-id="97344-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="97344-115">As funções [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) são opcionais.</span><span class="sxs-lookup"><span data-stu-id="97344-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="97344-116">A DLL de extensão pode exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) em vez de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) ou [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span><span class="sxs-lookup"><span data-stu-id="97344-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="97344-117">Se a DLL de extensão exportar [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), ela também deverá exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span><span class="sxs-lookup"><span data-stu-id="97344-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="97344-118">Definido pelo sistema</span><span class="sxs-lookup"><span data-stu-id="97344-118">System Defined</span></span>

<span data-ttu-id="97344-119">Quando o NPS chama uma implementação de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), o NPS passa a função um ponteiro para uma estrutura de bloco de [**controle de \_ extensão \_ \_ RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .</span><span class="sxs-lookup"><span data-stu-id="97344-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="97344-120">A estrutura do [**\_ bloco de \_ controle \_ de extensão RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:</span><span class="sxs-lookup"><span data-stu-id="97344-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="97344-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="97344-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="97344-123">[**Setresponsetype**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="97344-124">As funções [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) retornam ponteiros para uma estrutura do tipo [**\_ \_ matriz de atributo RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span><span class="sxs-lookup"><span data-stu-id="97344-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="97344-125">A estrutura de [**\_ \_ matriz de atributo RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contém ponteiros de função para as seguintes funções fornecidas pelo NPS:</span><span class="sxs-lookup"><span data-stu-id="97344-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="97344-126">[**Adicionar**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="97344-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="97344-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="97344-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="97344-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="97344-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97344-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 