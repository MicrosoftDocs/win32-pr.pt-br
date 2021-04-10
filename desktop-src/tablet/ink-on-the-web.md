---
description: O kit de desenvolvimento do Windows Vista Software Development Kit e do Windows XP Tablet PC Edition permitem que você crie aplicativos Web habilitados para tinta para usuários do Tablet PC que devem acessar aplicativos remotos.
ms.assetid: 4ba1ab4b-57d2-40da-a7c7-2402f8845ff5
title: Tinta na Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3584fdc0f19cbf9ac1a60e8f1607971165077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090012"
---
# <a name="ink-on-the-web"></a><span data-ttu-id="a4a7c-103">Tinta na Web</span><span class="sxs-lookup"><span data-stu-id="a4a7c-103">Ink on the Web</span></span>

<span data-ttu-id="a4a7c-104">O kit de desenvolvimento do Windows Vista Software Development Kit e do Windows XP Tablet PC Edition permitem que você crie aplicativos Web habilitados para tinta para usuários do Tablet PC que devem acessar aplicativos remotos.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-104">The Windows Vista Software Development Kit and Windows XP Tablet PC Edition Development Kit allow you to create ink-enabled web applications for Tablet PC users who must access remote applications.</span></span> <span data-ttu-id="a4a7c-105">Há duas técnicas básicas para fazer isso: uma é uma implantação sem intervenção, que permite que os aplicativos .NET sejam implantados de um servidor de arquivos ou Web, e o outro é criar páginas da Web habilitadas para tinta com controles de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-105">There are two basic techniques for accomplishing this: one is no-touch deployment, which allows .NET applications to be deployed from a Web or file server, and the other is to create ink-enabled Web pages with Windows Forms controls.</span></span> <span data-ttu-id="a4a7c-106">Em ambos os casos, a tinta é tratada no cliente, e não no servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-106">In both cases, the ink is handled on the client, rather than the server.</span></span> <span data-ttu-id="a4a7c-107">Observe que a API COM não tem suporte para a Web.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-107">Note that the COM API is not supported for the Web.</span></span>

<span data-ttu-id="a4a7c-108">Para usar o processamento do lado do cliente na Web, você precisa entender o modelo de segurança do .NET e como operar sob confiança parcial afeta seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-108">To use client-side processing over the Web, you need to understand the .NET security model and how operating under partial trust affects your application.</span></span> <span data-ttu-id="a4a7c-109">Por esse motivo, a segurança e a confiança para aplicativos do Tablet PC também são discutidas.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-109">For this reason, security and trust for Tablet PC applications is discussed as well.</span></span>

<span data-ttu-id="a4a7c-110">Os tópicos a seguir contêm observações sobre várias maneiras de criar aplicativos Web habilitados para tinta.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-110">The following topics contain notes on various ways of creating ink-enabled Web applications.</span></span>

-   [<span data-ttu-id="a4a7c-111">Nenhuma implantação por toque</span><span class="sxs-lookup"><span data-stu-id="a4a7c-111">No Touch Deployment</span></span>](no-touch-deployment.md)
-   [<span data-ttu-id="a4a7c-112">Controles da Web</span><span class="sxs-lookup"><span data-stu-id="a4a7c-112">Web Controls</span></span>](web-controls.md)
-   [<span data-ttu-id="a4a7c-113">Aplicativos Web habilitados para tinta</span><span class="sxs-lookup"><span data-stu-id="a4a7c-113">Ink-Enabled Web Applications</span></span>](ink-enabled-web-applications.md)
-   [<span data-ttu-id="a4a7c-114">Segurança e confiança</span><span class="sxs-lookup"><span data-stu-id="a4a7c-114">Security and Trust</span></span>](security-and-trust.md)

 

 



