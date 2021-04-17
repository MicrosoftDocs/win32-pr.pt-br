---
description: Este tutorial destaca os diferentes aspectos aos quais os desenvolvedores da Web devem se preocupar ao criar páginas para o fluxo de autorização da Web para o Windows 8. Esta seção mostra um fluxo de autorização de duas páginas.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Tutorial para autenticação de páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752620"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="0fa28-104">Tutorial para autenticação de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="0fa28-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="0fa28-105">Este tutorial destaca os diferentes aspectos aos quais os desenvolvedores da Web devem se preocupar ao criar páginas para o fluxo de autorização da Web para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0fa28-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="0fa28-106">Esta seção mostra um fluxo de autorização de duas páginas.</span><span class="sxs-lookup"><span data-stu-id="0fa28-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="0fa28-107">**Objetivo:** O objetivo do exemplo é não ser prescritiva sobre o layout ou o design visual que, com certeza, cada provedor terá um ponto de vista exclusivo, mas para destacar algumas áreas que valem a pena investir em ter uma experiência de estilo de design da Microsoft de primeira classe para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0fa28-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0fa28-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0fa28-108">Prerequisites</span></span>

<span data-ttu-id="0fa28-109">Para usar as APIs do agente de autenticação da Web, você precisa:</span><span class="sxs-lookup"><span data-stu-id="0fa28-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="0fa28-110">Windows 8 (somente x86 ou AMD64)</span><span class="sxs-lookup"><span data-stu-id="0fa28-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="0fa28-111">O Microsoft Serviços de Informações da Internet (IIS) deve ser instalado no painel de controle em "programas e recursos" e usando a opção "ativar ou desativar recursos do Windows".</span><span class="sxs-lookup"><span data-stu-id="0fa28-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="0fa28-112">**Tempo total para conclusão:** 2 minutos.</span><span class="sxs-lookup"><span data-stu-id="0fa28-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="0fa28-113">Para onde ir a partir de agora</span><span class="sxs-lookup"><span data-stu-id="0fa28-113">Where to go from here</span></span>

<span data-ttu-id="0fa28-114">Próxima [autenticação para páginas da Web](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="0fa28-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fa28-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fa28-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fa28-116">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="0fa28-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="0fa28-117">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="0fa28-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="0fa28-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="0fa28-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
