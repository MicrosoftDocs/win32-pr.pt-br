---
description: Este documento fornece informações sobre considerações de segurança relacionadas à WIA (aquisição de imagens do Windows).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considerações de segurança: aquisição de imagem do Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807939"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="84813-103">Considerações de segurança: aquisição de imagem do Windows</span><span class="sxs-lookup"><span data-stu-id="84813-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="84813-104">Este documento fornece informações sobre considerações de segurança relacionadas à WIA (aquisição de imagens do Windows).</span><span class="sxs-lookup"><span data-stu-id="84813-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="84813-105">Este documento não fornece tudo o que você precisa saber sobre problemas de segurança. em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="84813-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="84813-106">Usar aspas ao contrário dos nomes de caminho</span><span class="sxs-lookup"><span data-stu-id="84813-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="84813-107">Coloque os aplicativos registrados em locais seguros</span><span class="sxs-lookup"><span data-stu-id="84813-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="84813-108">Não usar diretórios subjacentes ou chaves do registro</span><span class="sxs-lookup"><span data-stu-id="84813-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="84813-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84813-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="84813-110">Usar aspas ao contrário dos nomes de caminho</span><span class="sxs-lookup"><span data-stu-id="84813-110">Use quotation marks around path names</span></span>

<span data-ttu-id="84813-111">Ao usar [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar um aplicativo para receber eventos de dispositivo, certifique-se de colocar o caminho e o nome de arquivo do aplicativo entre aspas.</span><span class="sxs-lookup"><span data-stu-id="84813-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="84813-112">Isso evita a possibilidade de o caminho ser interpretado erroneamente e um aplicativo não autorizado ser executado.</span><span class="sxs-lookup"><span data-stu-id="84813-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="84813-113">Coloque os aplicativos registrados em locais seguros</span><span class="sxs-lookup"><span data-stu-id="84813-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="84813-114">Quando um aplicativo é registrado para receber um evento de dispositivo, esse aplicativo pode ser executado por qualquer usuário que tenha acesso a esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84813-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="84813-115">Por exemplo, se um aplicativo for registrado para um evento de verificação, pressionar o botão "Scan" em um scanner fará com que esse aplicativo seja executado.</span><span class="sxs-lookup"><span data-stu-id="84813-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="84813-116">Se o aplicativo for executado com um privilégio maior do que o usuário, isso causará um possível problema de segurança.</span><span class="sxs-lookup"><span data-stu-id="84813-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="84813-117">Não usar diretórios subjacentes ou chaves do registro</span><span class="sxs-lookup"><span data-stu-id="84813-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="84813-118">O WIA usa vários diretórios e chaves de registro internamente para armazenar dados ou informações.</span><span class="sxs-lookup"><span data-stu-id="84813-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="84813-119">Não acesse esses diretórios ou chaves do registro diretamente.</span><span class="sxs-lookup"><span data-stu-id="84813-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="84813-120">Em vez disso, use os métodos de interface expostos para especificar diretórios para imagens adquiridas.</span><span class="sxs-lookup"><span data-stu-id="84813-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84813-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84813-121">Related Topics</span></span>

-   [<span data-ttu-id="84813-122">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="84813-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="84813-123">Home Page de segurança da biblioteca MSDN</span><span class="sxs-lookup"><span data-stu-id="84813-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="84813-124">Recursos de instruções de segurança</span><span class="sxs-lookup"><span data-stu-id="84813-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="84813-125">Recursos de segurança do TechNet</span><span class="sxs-lookup"><span data-stu-id="84813-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="84813-126">[Considerações de segurança para desenvolvedores do Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="84813-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="84813-127">Práticas recomendadas de segurança</span><span class="sxs-lookup"><span data-stu-id="84813-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
