---
title: Diretrizes de programação de Serviços de Área de Trabalho Remota
description: Tópicos que fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, diretrizes de programação
- Diretrizes de programação Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105778805"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="b8e03-105">Diretrizes de programação de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b8e03-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="b8e03-106">A maioria dos aplicativos baseados no Windows de 32 bits ou 64 bits executam "no estado em que se encontram" em um ambiente Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal).</span><span class="sxs-lookup"><span data-stu-id="b8e03-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="b8e03-107">No entanto, alguns aplicativos funcionam corretamente e funcionam bem em um ambiente de Serviços de Área de Trabalho Remota, enquanto outros não.</span><span class="sxs-lookup"><span data-stu-id="b8e03-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="b8e03-108">Os tópicos a seguir fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b8e03-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b8e03-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b8e03-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b8e03-110">Diretrizes de vários usuários</span><span class="sxs-lookup"><span data-stu-id="b8e03-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="b8e03-111">Diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b8e03-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b8e03-112">Diretrizes de desempenho</span><span class="sxs-lookup"><span data-stu-id="b8e03-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="b8e03-113">Diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b8e03-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b8e03-114">Diretrizes gerais de programação</span><span class="sxs-lookup"><span data-stu-id="b8e03-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="b8e03-115">Diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b8e03-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="b8e03-116">Muitas dessas diretrizes são boas práticas de programação que irão beneficiar os aplicativos em execução em qualquer ambiente do Windows.</span><span class="sxs-lookup"><span data-stu-id="b8e03-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="b8e03-117">No entanto, algumas otimizações recomendadas, como a limitação de efeitos gráficos, são otimizações que você desejará apenas quando o aplicativo estiver sendo executado em Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b8e03-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="b8e03-118">Para obter um exemplo de código que mostra como detectar um ambiente de Serviços de Área de Trabalho Remota, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b8e03-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8e03-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8e03-119">Related topics</span></span>

<dl> <span data-ttu-id="b8e03-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b8e03-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b8e03-121">Os serviços de terminal agora estão Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b8e03-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="b8e03-122">Formato de arquivo de modelo administrativo</span><span class="sxs-lookup"><span data-stu-id="b8e03-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="b8e03-123">Segurança da chave do registro e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e03-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="b8e03-124">Hives do registro</span><span class="sxs-lookup"><span data-stu-id="b8e03-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="b8e03-125">Descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="b8e03-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="b8e03-126">Direitos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="b8e03-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="b8e03-127">Modelo de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e03-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 