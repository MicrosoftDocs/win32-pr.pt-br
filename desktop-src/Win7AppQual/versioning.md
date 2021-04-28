---
description: Controle de versão (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Controle de versão (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103694"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="c54f7-103">Controle de versão (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="c54f7-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="c54f7-104">Um dos problemas mais comuns de compatibilidade de aplicativos para o Windows Internet Explorer são as cadeias de caracteres do agente do usuário (UA) e os vetores de versão.</span><span class="sxs-lookup"><span data-stu-id="c54f7-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="c54f7-105">O Windows Internet Explorer 8 apresenta uma nova cadeia de caracteres de UA para ajudar os aplicativos a detectar qual versão os usuários estão executando.</span><span class="sxs-lookup"><span data-stu-id="c54f7-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="c54f7-106">Além de simplesmente aumentar o valor de MSIE associado ao Internet Explorer na cadeia de caracteres UA, o Internet Explorer 8 adiciona um valor Trident/4.0 para ajudá-lo a detectar se o Internet Explorer 8 está sendo executado no modo de exibição de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="c54f7-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="c54f7-107">Essas alterações, além de verificações de versão codificadas, podem apresentar problemas de compatibilidade entre navegadores.</span><span class="sxs-lookup"><span data-stu-id="c54f7-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c54f7-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c54f7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c54f7-109">Atualizações de design que afetam a compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="c54f7-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



