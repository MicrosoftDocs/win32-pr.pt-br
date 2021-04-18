---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: DISM (Gerenciamento e Manutenção de Imagens de Implantação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788680"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="bfa2c-103">DISM (Gerenciamento e Manutenção de Imagens de Implantação)</span><span class="sxs-lookup"><span data-stu-id="bfa2c-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="bfa2c-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="bfa2c-104">Affected Platforms</span></span>

<span data-ttu-id="bfa2c-105">**Clientes** -Windows Vista SP1 e \| Windows 7 posterior</span><span class="sxs-lookup"><span data-stu-id="bfa2c-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="bfa2c-106">**Servidores** -windows Server 2008 RTM e posterior \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfa2c-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="bfa2c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfa2c-107">Description</span></span>

<span data-ttu-id="bfa2c-108">A ferramenta DISM (gerenciamento e manutenção de imagens de implantação) substitui as ferramentas pkgmgr, PEImg e IntlConfg que estão sendo desativadas no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="bfa2c-109">O DISM fornece uma única ferramenta centralizada para executar todas as funções dessas três ferramentas de maneira mais eficiente e padronizada, eliminando a origem de muitas das frustrações experimentadas pelos usuários atuais dessas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="bfa2c-110">O DISM inclui um Shim para o Windows Vista SP1 e posterior, bem como para o Windows Server 2008 RTM e posterior, que redireciona as chamadas de pkgmgr de aplicativos herdados em execução no Windows 7 para o DISM.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="bfa2c-111">Se o aplicativo estiver em execução em um dos sistemas operacionais com suporte, o Shim roteará a chamada para Pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="bfa2c-112">Não existem correções para aplicativos herdados que chamam PEImg ou IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="bfa2c-113">Uso</span><span class="sxs-lookup"><span data-stu-id="bfa2c-113">Usage</span></span>

<span data-ttu-id="bfa2c-114">O DISM é transparente para os usuários finais de pkgmgr em qualquer uma das plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="bfa2c-115">No entanto, se um aplicativo chamar o PEImg ou o IntlConfg do Windows 7, a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="bfa2c-116">Atualize todos os scripts que chamam pkgmgr, PEImg ou IntlConfg para chamar o DISM em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="bfa2c-117">É importante incluir a atualização de scripts do pkgmgr nesse esforço, já que o Shim que fornece compatibilidade com versões anteriores para o pkgmgr será removido em versões futuras dos sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="bfa2c-118">Verifique se as chamadas para o DISM substituiram todas as chamadas para pkgmgr, PEImg e IntlConfg, e se a operação é executada com êxito.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfa2c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfa2c-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bfa2c-120">[Gerenciamento e manutenção de imagens de implantação (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bfa2c-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
