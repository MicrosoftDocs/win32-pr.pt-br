---
title: Usando extensões do NPS
description: Saiba mais sobre como usar as extensões do NPS. O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS, tarefas do serviço de autenticação da Internet
- Serviço de autenticação da Internet IAS, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989063"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="09886-106">Usando extensões do NPS</span><span class="sxs-lookup"><span data-stu-id="09886-106">Using NPS Extensions</span></span>

<span data-ttu-id="09886-107">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).</span><span class="sxs-lookup"><span data-stu-id="09886-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="09886-108">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="09886-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="09886-109">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="09886-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="09886-110">\* \* Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="09886-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="09886-111">Os exemplos de Diale e MapName estendem a funcionalidade do NPS.</span><span class="sxs-lookup"><span data-stu-id="09886-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="09886-112">Amostra</span><span class="sxs-lookup"><span data-stu-id="09886-112">Sample</span></span>             | <span data-ttu-id="09886-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="09886-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09886-114">Conexão</span><span class="sxs-lookup"><span data-stu-id="09886-114">DialIn</span></span><br/>  | <span data-ttu-id="09886-115">Este exemplo implementa uma extensão RADIUS DLL que verifica o bit de discagem para o usuário.</span><span class="sxs-lookup"><span data-stu-id="09886-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="09886-116">MapName</span><span class="sxs-lookup"><span data-stu-id="09886-116">MapName</span></span><br/> | <span data-ttu-id="09886-117">Esta DLL de extensão de exemplo pesquisa todos os domínios confiáveis para a conta designada.</span><span class="sxs-lookup"><span data-stu-id="09886-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="09886-118">Isso permite que os usuários de vários domínios sejam autenticados sem que os usuários precisem fornecer seu nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="09886-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="09886-119">Você pode encontrar o código-fonte para os aplicativos de exemplo MapName e dial-in na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="09886-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="09886-120">*Local*,% caminho de instalação%, designa o diretório de instalação base para computadores x64.</span><span class="sxs-lookup"><span data-stu-id="09886-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="09886-121">Consulte também [Windows Software Development Kit (SDK) para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), SDK (Software Development Kit) do Microsoft Windows e [downloads para o desenvolvimento de aplicativos da Windows Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="09886-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="09886-122">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="09886-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="09886-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09886-123">Windows Server 2012</span></span>

<span data-ttu-id="09886-124">Link de download: N/A</span><span class="sxs-lookup"><span data-stu-id="09886-124">Download link: N/A</span></span>

<span data-ttu-id="09886-125">MapName: não</span><span class="sxs-lookup"><span data-stu-id="09886-125">MapName: No</span></span>

<span data-ttu-id="09886-126">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="09886-126">DialIn: No</span></span>

<span data-ttu-id="09886-127">Local: N/A</span><span class="sxs-lookup"><span data-stu-id="09886-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="09886-128">SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="09886-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="09886-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09886-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="09886-130">Link de download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="09886-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="09886-131">MapName: Sim</span><span class="sxs-lookup"><span data-stu-id="09886-131">MapName: Yes</span></span>

<span data-ttu-id="09886-132">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="09886-132">DialIn: No</span></span>

<span data-ttu-id="09886-133">Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 7.1 \\ Samples \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="09886-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="09886-134">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="09886-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="09886-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09886-135">Windows Server 2008</span></span>

<span data-ttu-id="09886-136">Link de download: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="09886-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="09886-137">MapName: Sim</span><span class="sxs-lookup"><span data-stu-id="09886-137">MapName: Yes</span></span>

<span data-ttu-id="09886-138">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="09886-138">DialIn: No</span></span>

<span data-ttu-id="09886-139">Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ ias</span><span class="sxs-lookup"><span data-stu-id="09886-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="09886-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09886-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09886-141">Downloads para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="09886-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="09886-142">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="09886-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





