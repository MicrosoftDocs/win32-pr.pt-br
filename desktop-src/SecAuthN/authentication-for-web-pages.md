---
description: A autenticação está comprovando quem você é.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticação para páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922371"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="a121c-103">Autenticação para páginas da Web</span><span class="sxs-lookup"><span data-stu-id="a121c-103">Authentication for web pages</span></span>

<span data-ttu-id="a121c-104">A autenticação está comprovando quem você é.</span><span class="sxs-lookup"><span data-stu-id="a121c-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="a121c-105">**Objetivo:** Para que o agente de autenticação da Web seja exibido como parte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a121c-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a121c-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a121c-106">Prerequisites</span></span>

<span data-ttu-id="a121c-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a121c-107">None</span></span>

<span data-ttu-id="a121c-108">**Tempo para concluir:** 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="a121c-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="a121c-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="a121c-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="a121c-110">1. Introdução</span><span class="sxs-lookup"><span data-stu-id="a121c-110">1. Getting started</span></span>

<span data-ttu-id="a121c-111">Inicie o arquivo de instalação para instalar um site contoso no Serviços de Informações da Internet 8 no computador local para hospedar os arquivos HTML e CSS de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a121c-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="a121c-112">Os arquivos HTML e CSS de exemplo serão instalados no diretório arquivos de programas do Microsoft \\ contoso.</span><span class="sxs-lookup"><span data-stu-id="a121c-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="a121c-113">Além disso, um aplicativo da Windows Store "fabrikam social" será desempacotado na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a121c-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="a121c-114">2. familiarizando-se</span><span class="sxs-lookup"><span data-stu-id="a121c-114">2. Getting familiar</span></span>

<span data-ttu-id="a121c-115">Para ter uma ideia de como as páginas de exemplo se parecem no agente de autenticação da Web, abra o arquivo de solução Fabrikam social do Visual Studio 11 na pasta "fabrikam social" na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a121c-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="a121c-116">Execute o aplicativo e clique em "Iniciar" para abrir as páginas de exemplo no agente de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="a121c-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="a121c-117">O aplicativo pode ser redimensionado para um lado ou ativado por meio do compartilhamento de alguns dados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a121c-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="a121c-118">3. autenticação</span><span class="sxs-lookup"><span data-stu-id="a121c-118">3. Authentication</span></span>

<span data-ttu-id="a121c-119">Quando a API de autenticação da Web é invocada pelo aplicativo subjacente para se conectar ao provedor, "contoso social", a página de logon é mostrada.</span><span class="sxs-lookup"><span data-stu-id="a121c-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="a121c-120">Esta página foi projetada para ser melhor em uma experiência de logon rápida e fluida.</span><span class="sxs-lookup"><span data-stu-id="a121c-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="a121c-121">Ele também fornece pontos de entrada para algumas outras ações comuns do usuário, como recuperar detalhes da senha, inscrever-se em uma conta e ler instruções sobre privacidade e termos e condições que são concluídas no navegador.</span><span class="sxs-lookup"><span data-stu-id="a121c-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![página de logon da contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="a121c-123">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a121c-123">Summary and next steps</span></span>

<span data-ttu-id="a121c-124">[Tutorial de resumo para autenticação de páginas da Web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="a121c-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="a121c-125">Próxima [autorização para páginas da Web](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="a121c-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a121c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a121c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a121c-127">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="a121c-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="a121c-128">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="a121c-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="a121c-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="a121c-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
