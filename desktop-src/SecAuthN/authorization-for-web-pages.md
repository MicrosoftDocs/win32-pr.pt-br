---
description: A autorização define a quais recursos você tem acesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorização para páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827597"
---
# <a name="authorization-for-web-pages"></a><span data-ttu-id="b0c16-103">Autorização para páginas da Web</span><span class="sxs-lookup"><span data-stu-id="b0c16-103">Authorization for web pages</span></span>

<span data-ttu-id="b0c16-104">A autorização define a quais recursos você tem acesso.</span><span class="sxs-lookup"><span data-stu-id="b0c16-104">Authorization sets what resources you have access to.</span></span>

<span data-ttu-id="b0c16-105">**Objetivo:** Para permitir que os usuários acessem seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0c16-105">**Objective:** To allow users access to your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b0c16-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b0c16-106">Prerequisites</span></span>

<span data-ttu-id="b0c16-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b0c16-107">None</span></span>

<span data-ttu-id="b0c16-108">**Tempo para conclusão:** 2 minutos.</span><span class="sxs-lookup"><span data-stu-id="b0c16-108">**Time to complete:** 2 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="b0c16-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="b0c16-109">Instructions</span></span>

### <a name="1-authorization"></a><span data-ttu-id="b0c16-110">1. autorização</span><span class="sxs-lookup"><span data-stu-id="b0c16-110">1. Authorization</span></span>

<span data-ttu-id="b0c16-111">Quando o usuário insere suas credenciais e clica no botão de logon, a página permissões é mostrada.</span><span class="sxs-lookup"><span data-stu-id="b0c16-111">When the user enters their credentials and clicks the Login button, the permissions page is shown.</span></span> <span data-ttu-id="b0c16-112">Essa página é melhor para permitir que os usuários controlem as permissões granulares ao conceder ao aplicativo acesso aos dados da contoso.</span><span class="sxs-lookup"><span data-stu-id="b0c16-112">This page is best at allowing users to control granular permissions in granting the app to access to Contoso’s data.</span></span> ![página de permissões da contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a><span data-ttu-id="b0c16-114">2. como usar o exemplo</span><span class="sxs-lookup"><span data-stu-id="b0c16-114">2. How to use the sample</span></span>

<span data-ttu-id="b0c16-115">Você precisa saber sobre os seguintes arquivos HTML e CSS.</span><span class="sxs-lookup"><span data-stu-id="b0c16-115">You need to know about the following HTML and CSS files.</span></span>

1.  <span data-ttu-id="b0c16-116">Os seguintes arquivos HTML correspondem às duas páginas no fluxo de autorização da Web</span><span class="sxs-lookup"><span data-stu-id="b0c16-116">The following HTML files correspond to the two pages in the web authorization flow</span></span>
    -   <span data-ttu-id="b0c16-117">WebAuthLogin.html – HTML de exemplo para a página de logon</span><span class="sxs-lookup"><span data-stu-id="b0c16-117">WebAuthLogin.html – sample HTML for the login page</span></span>
    -   <span data-ttu-id="b0c16-118">WebAuthPermissions.html – HTML de exemplo para a página de permissões</span><span class="sxs-lookup"><span data-stu-id="b0c16-118">WebAuthPermissions.html – sample HTML for the permissions page</span></span>
2.  <span data-ttu-id="b0c16-119">Os arquivos CSS contêm estilos do Windows 8 para ajudar a criar uma página da Web do aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b0c16-119">The CSS files contain Windows 8 styles to help create a Windows Store app web page.</span></span>
    -   <span data-ttu-id="b0c16-120">UI-Light. css – isso foi derivado da folha de estilos base para controles do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b0c16-120">ui-light.css – this has been derived from the base style sheet for Windows 8 controls.</span></span>
    -   <span data-ttu-id="b0c16-121">UI-webauth. css – fornece estilo incremental para otimizar o layout para páginas de autenticação na Web.</span><span class="sxs-lookup"><span data-stu-id="b0c16-121">ui-webauth.css – this provides incremental styling for optimizing layout for web auth pages.</span></span>
    -   <span data-ttu-id="b0c16-122">Theme-Colors. css – fornece o estilo incremental para substituir as cores de destaque padrão dos controles pela cor da marca do provedor.</span><span class="sxs-lookup"><span data-stu-id="b0c16-122">theme-colors.css – this provides the incremental styling to override default accent colors of controls with the provider’s brand color.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="b0c16-123">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b0c16-123">Summary and next steps</span></span>

<span data-ttu-id="b0c16-124">[Tutorial de resumo para autenticação de páginas da Web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="b0c16-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="b0c16-125">Próximas [práticas recomendadas para a criação de páginas da Web de autenticação](best-practices-for-designing-authentication-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="b0c16-125">Next [Best practices for designing authentication web pages](best-practices-for-designing-authentication-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0c16-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0c16-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0c16-127">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="b0c16-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="b0c16-128">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="b0c16-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="b0c16-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="b0c16-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
