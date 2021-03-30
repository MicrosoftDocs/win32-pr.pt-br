---
title: Ferramenta de teste pronto para plataforma Microsoft
description: Ferramenta de teste pronto para plataforma Microsoft
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641956"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="754ef-103">Ferramenta de teste pronto para plataforma Microsoft</span><span class="sxs-lookup"><span data-stu-id="754ef-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="754ef-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="754ef-104">Platform</span></span>

 <span data-ttu-id="754ef-105">**Servidores** – windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="754ef-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="754ef-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="754ef-106">Description</span></span>

<span data-ttu-id="754ef-107">A ferramenta de teste Microsoft Platform Ready (MPR) Test é usada para a preparação do aplicativo da plataforma e para validar a conformidade com os requisitos de certificação para aplicativos do Windows Server 2012 e do Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="754ef-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="754ef-108">A Microsoft incentiva enfaticamente a incorporação da ferramenta de teste de MPR aos processos de criação e teste de software, garantindo assim a prontidão da plataforma antes que os aplicativos sejam lançados no mercado.</span><span class="sxs-lookup"><span data-stu-id="754ef-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="754ef-109">A ferramenta de teste de MPR também é uma ferramenta recomendada para testar aplicativos de linha de negócios e para avaliar os produtos de servidor para a compatibilidade da plataforma antes de tomar decisões de compra.</span><span class="sxs-lookup"><span data-stu-id="754ef-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="754ef-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="754ef-110">Requirements</span></span>

<span data-ttu-id="754ef-111">A ferramenta de teste de MPR inclui testes automatizados para o:</span><span class="sxs-lookup"><span data-stu-id="754ef-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="754ef-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="754ef-112">Windows Installer</span></span>
-   <span data-ttu-id="754ef-113">Configuração e funcionalidade primária</span><span class="sxs-lookup"><span data-stu-id="754ef-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="754ef-114">Drivers e segurança</span><span class="sxs-lookup"><span data-stu-id="754ef-114">Drivers and Security</span></span>
-   <span data-ttu-id="754ef-115">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="754ef-115">Best Practices</span></span>

<span data-ttu-id="754ef-116">O teste automático e o envio de resultados para a maioria dos aplicativos de servidor devem levar 2 horas ou menos; aplicativos mais complexos podem levar cerca de 4 horas.</span><span class="sxs-lookup"><span data-stu-id="754ef-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="754ef-117">Todos os drivers devem passar separadamente no teste de certificação de hardware do Windows e ser assinados pela Microsoft para o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="754ef-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="754ef-118">Uso</span><span class="sxs-lookup"><span data-stu-id="754ef-118">Usage</span></span>

<span data-ttu-id="754ef-119">Para testar seus aplicativos:</span><span class="sxs-lookup"><span data-stu-id="754ef-119">To test your apps:</span></span>

1.  <span data-ttu-id="754ef-120">Instale a configuração mínima mais recente do Windows Server 2012 (GUI do servidor completo, interface mínima do servidor ou núcleo do servidor) conforme necessário para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="754ef-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="754ef-121">Examine os requisitos de certificação.</span><span class="sxs-lookup"><span data-stu-id="754ef-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="754ef-122">Em um sistema limpo, execute a ferramenta de teste MPR no modo de interface do usuário completa ou no modo de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="754ef-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="754ef-123">Conclua o processo de teste autoguiado.</span><span class="sxs-lookup"><span data-stu-id="754ef-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="754ef-124">Examine os resultados e corrija seu aplicativo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="754ef-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="754ef-125">Entre e carregue os resultados bem-sucedidos no portal pronto para a plataforma Microsoft para obter uma listagem no catálogo do Windows Server e no uso do logotipo.</span><span class="sxs-lookup"><span data-stu-id="754ef-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="754ef-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="754ef-126">Resources</span></span>

-   [<span data-ttu-id="754ef-127">Requisitos para o programa de certificação de aplicativos do Windows Server</span><span class="sxs-lookup"><span data-stu-id="754ef-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="754ef-128">Ferramenta de teste da plataforma Microsoft Ready (MPR)</span><span class="sxs-lookup"><span data-stu-id="754ef-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="754ef-129">Programa de certificação de aplicativos do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="754ef-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="754ef-130">Comentários sobre o logotipo do Windows Server</span><span class="sxs-lookup"><span data-stu-id="754ef-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 