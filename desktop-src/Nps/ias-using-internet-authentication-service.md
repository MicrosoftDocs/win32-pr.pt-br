---
title: Usando extensões do NPS
description: O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS, tarefas do serviço de autenticação da Internet
- Serviço de autenticação da Internet IAS, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104499008"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="10d86-105">Usando extensões do NPS</span><span class="sxs-lookup"><span data-stu-id="10d86-105">Using NPS Extensions</span></span>

<span data-ttu-id="10d86-106">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).</span><span class="sxs-lookup"><span data-stu-id="10d86-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="10d86-107">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="10d86-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="10d86-108">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="10d86-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="10d86-109">\* \* Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="10d86-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="10d86-110">Os exemplos de Diale e MapName estendem a funcionalidade do NPS.</span><span class="sxs-lookup"><span data-stu-id="10d86-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="10d86-111">Amostra</span><span class="sxs-lookup"><span data-stu-id="10d86-111">Sample</span></span>             | <span data-ttu-id="10d86-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="10d86-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d86-113">Conexão</span><span class="sxs-lookup"><span data-stu-id="10d86-113">DialIn</span></span><br/>  | <span data-ttu-id="10d86-114">Este exemplo implementa uma extensão RADIUS DLL que verifica o bit de discagem para o usuário.</span><span class="sxs-lookup"><span data-stu-id="10d86-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="10d86-115">MapName</span><span class="sxs-lookup"><span data-stu-id="10d86-115">MapName</span></span><br/> | <span data-ttu-id="10d86-116">Esta DLL de extensão de exemplo pesquisa todos os domínios confiáveis para a conta designada.</span><span class="sxs-lookup"><span data-stu-id="10d86-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="10d86-117">Isso permite que os usuários de vários domínios sejam autenticados sem que os usuários precisem fornecer seu nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="10d86-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="10d86-118">Você pode encontrar o código-fonte para os aplicativos de exemplo MapName e dial-in na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="10d86-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="10d86-119">*Local*,% caminho de instalação%, designa o diretório de instalação base para computadores x64.</span><span class="sxs-lookup"><span data-stu-id="10d86-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="10d86-120">Consulte também [Windows Software Development Kit (SDK) para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), SDK (Software Development Kit) do Microsoft Windows e [downloads para o desenvolvimento de aplicativos da Windows Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="10d86-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="10d86-121">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="10d86-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="10d86-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10d86-122">Windows Server 2012</span></span>

<span data-ttu-id="10d86-123">Link de download: N/A</span><span class="sxs-lookup"><span data-stu-id="10d86-123">Download link: N/A</span></span>

<span data-ttu-id="10d86-124">MapName: não</span><span class="sxs-lookup"><span data-stu-id="10d86-124">MapName: No</span></span>

<span data-ttu-id="10d86-125">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="10d86-125">DialIn: No</span></span>

<span data-ttu-id="10d86-126">Local: N/A</span><span class="sxs-lookup"><span data-stu-id="10d86-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="10d86-127">SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="10d86-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="10d86-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10d86-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="10d86-129">Link de download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="10d86-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="10d86-130">MapName: Sim</span><span class="sxs-lookup"><span data-stu-id="10d86-130">MapName: Yes</span></span>

<span data-ttu-id="10d86-131">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="10d86-131">DialIn: No</span></span>

<span data-ttu-id="10d86-132">Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 7.1 \\ Samples \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="10d86-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="10d86-133">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="10d86-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="10d86-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d86-134">Windows Server 2008</span></span>

<span data-ttu-id="10d86-135">Link de download: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="10d86-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="10d86-136">MapName: Sim</span><span class="sxs-lookup"><span data-stu-id="10d86-136">MapName: Yes</span></span>

<span data-ttu-id="10d86-137">Conexão: não</span><span class="sxs-lookup"><span data-stu-id="10d86-137">DialIn: No</span></span>

<span data-ttu-id="10d86-138">Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ ias</span><span class="sxs-lookup"><span data-stu-id="10d86-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="10d86-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10d86-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d86-140">Downloads para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="10d86-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="10d86-141">SDK do Windows para Windows 8</span><span class="sxs-lookup"><span data-stu-id="10d86-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





