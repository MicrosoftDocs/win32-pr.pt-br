---
description: Diretrizes para desenvolvedores da Web e provedores online para criar páginas da Web adaptadas para as APIs do agente de autenticação da Web do Windows 8 para recursos de logon único (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Diretrizes de introdução para provedores online integração com as APIs do agente de autenticação da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829462"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="87636-103">Diretrizes de introdução para provedores online integração com as APIs do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="87636-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="87636-104">Esta seção orienta os desenvolvedores da Web e os provedores online para a criação de páginas da Web adaptadas para as APIs do agente de autenticação da Web do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87636-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="87636-105">Ele fornece as recomendações visuais e interativas para uma experiência de usuário de ponta a ponta da página da Web, além de como habilitar os recursos de SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="87636-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87636-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="87636-106">In this section</span></span>



| <span data-ttu-id="87636-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="87636-107">Topic</span></span>                                                                                                     | <span data-ttu-id="87636-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="87636-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87636-109">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="87636-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="87636-110">O agente de autenticação da Web é criado na parte superior das mesmas tecnologias que alimentam o Internet Explorer no Windows.</span><span class="sxs-lookup"><span data-stu-id="87636-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="87636-111">No entanto, devido a uma finalidade muito especial desse componente, alguns recursos do Internet Explorer foram desabilitados ou bloqueados para configuração específica.</span><span class="sxs-lookup"><span data-stu-id="87636-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="87636-112">Como personalizar os elementos da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="87636-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="87636-113">Uma página da Web personaliza a interface do usuário com o título, o ícone e a cor do cabeçalho usando as marcas de metadados definidas na página da Web.</span><span class="sxs-lookup"><span data-stu-id="87636-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="87636-114">Tutorial para autenticação de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="87636-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="87636-115">Problemas de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="87636-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="87636-116">Este tópico descreve as dicas de solução de problemas para usar as APIs do agente de autenticação da Web para suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="87636-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="87636-117">Perguntas frequentes sobre o agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="87636-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="87636-118">Perguntas frequentes sobre o agente de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="87636-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="87636-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87636-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="87636-120">[Visão geral do agente de autenticação da Web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="87636-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="87636-121">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="87636-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="87636-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="87636-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

