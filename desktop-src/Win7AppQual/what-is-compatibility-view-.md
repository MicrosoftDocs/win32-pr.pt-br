---
description: O que é o modo de exibição de compatibilidade?
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: O que é o modo de exibição de compatibilidade?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be51f94d560d206c579d74d9407d53541205201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113394"
---
# <a name="what-is-compatibility-view"></a><span data-ttu-id="99dac-103">O que é o modo de exibição de compatibilidade?</span><span class="sxs-lookup"><span data-stu-id="99dac-103">What Is Compatibility View?</span></span>

<span data-ttu-id="99dac-104">A *exibição de compatibilidade* é um recurso do Windows Internet Explorer 8 que permite que o navegador processe uma página da Web quase idênticamente à forma como o Windows Internet Explorer 7 a processaria.</span><span class="sxs-lookup"><span data-stu-id="99dac-104">*Compatibility View* is a feature of Windows Internet Explorer 8 that enables the browser to render a webpage nearly identically to the way that Windows Internet Explorer 7 would render it.</span></span>

<span data-ttu-id="99dac-105">No Internet Explorer 8, a exibição de compatibilidade altera como o navegador interpreta o código escrito em CSS, HTML e o Modelo de Objeto do Documento (DOM) para tentar corresponder ao Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="99dac-105">In Internet Explorer 8, Compatibility View changes how the browser interprets code that is written in CSS, HTML, and the Document Object Model (DOM) to try to match Internet Explorer 7.</span></span> <span data-ttu-id="99dac-106">Um site que um usuário exibe no modo de exibição de compatibilidade do Internet Explorer 8 é quase idêntico a um site que o usuário exibe no Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="99dac-106">A site that a user views in Internet Explorer 8 Compatibility View is almost identical to a site that the user views in Internet Explorer 7.</span></span> <span data-ttu-id="99dac-107">No entanto, o modo de exibição de compatibilidade não altera como o navegador interpreta todo o código.</span><span class="sxs-lookup"><span data-stu-id="99dac-107">However, Compatibility View does not change how the browser interprets all code.</span></span> <span data-ttu-id="99dac-108">Por exemplo, as alterações no Internet Explorer 8 sobre como o navegador manipula o ActiveX, o analisador, o AJAX, o JavaScript, a rede e a segurança ainda podem causar problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="99dac-108">For example, the changes in Internet Explorer 8 for how the browser handles ActiveX, the parser, AJAX, JavaScript, networking, and security might still cause compatibility issues.</span></span> <span data-ttu-id="99dac-109">A exibição de compatibilidade não altera esses comportamentos.</span><span class="sxs-lookup"><span data-stu-id="99dac-109">Compatibility View does not change these behaviors.</span></span>

<span data-ttu-id="99dac-110">Em um ambiente corporativo, algumas áreas apresentam menor risco de problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="99dac-110">In an enterprise environment, some areas have lower risk for compatibility issues.</span></span> <span data-ttu-id="99dac-111">Por exemplo, sites da Zona da Intranet usam o Modo de Exibição de Compatibilidade por padrão.</span><span class="sxs-lookup"><span data-stu-id="99dac-111">For example, Intranet Zone websites use Compatibility View by default.</span></span> <span data-ttu-id="99dac-112">Os aplicativos Web do cliente que são renderizados usando o controle do navegador da Web ou o WebOC (mecanismo de renderização do Internet Explorer) também têm um baixo risco de problemas de compatibilidade, pois o Internet Explorer 8 usa como padrão um modo de compatibilidade para o WebOC.</span><span class="sxs-lookup"><span data-stu-id="99dac-112">Client web applications that render by using the Web Browser Control, or the WebOC (Internet Explorer rendering engine), also have a low risk for compatibility issues because Internet Explorer 8 defaults to a compatibility mode for the WebOC.</span></span> <span data-ttu-id="99dac-113">No entanto, as definições de configuração padrão para o modo de exibição de compatibilidade podem não garantir a compatibilidade completa.</span><span class="sxs-lookup"><span data-stu-id="99dac-113">However, the default configuration settings for Compatibility View might not ensure complete compatibility.</span></span> <span data-ttu-id="99dac-114">Para determinar se um site ou aplicativo Web é compatível com o Internet Explorer 8, você deve testar o site ou o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="99dac-114">To determine if a website or web application is compatible with Internet Explorer 8, you should test the website or web application.</span></span>

<span data-ttu-id="99dac-115">Para obter mais informações sobre as diferenças entre o modo de exibição de compatibilidade do Internet Explorer 8 e o Internet Explorer 7, consulte o [blog compatibilidade do site e o Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).</span><span class="sxs-lookup"><span data-stu-id="99dac-115">For more information about the differences between Internet Explorer 8 Compatibility View and Internet Explorer 7, see the [Site Compatibility and Internet Explorer 8 blog](/archive/blogs/ie/site-compatibility-and-ie8).</span></span> <span data-ttu-id="99dac-116">Para obter uma lista do que verificar ao atualizar para o Internet Explorer 8, consulte o [Kit de ferramentas de preparação para o Internet Explorer 8](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).</span><span class="sxs-lookup"><span data-stu-id="99dac-116">For a list of what to check when you upgrade to Internet Explorer 8, see the [Internet Explorer 8 Readiness Toolkit](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).</span></span>

<span data-ttu-id="99dac-117">Para obter mais informações sobre o modo de exibição de compatibilidade, consulte o [blog da equipe do Internet Explorer](/archive/blogs/ie/).</span><span class="sxs-lookup"><span data-stu-id="99dac-117">For more information about Compatibility View, see the [Internet Explorer Team Blog](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99dac-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99dac-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99dac-119">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="99dac-119">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
