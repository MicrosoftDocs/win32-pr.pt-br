---
description: Visão geral dos problemas de confiança parcial e da API (interface de programação de aplicativo) do StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considerações de confiança parcial para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170691"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a><span data-ttu-id="0c5cc-103">Considerações de confiança parcial para a API StylusInput</span><span class="sxs-lookup"><span data-stu-id="0c5cc-103">Partial Trust Considerations for the StylusInput API</span></span>

<span data-ttu-id="0c5cc-104">O [**RealTimeStylus**](realtimestylus-class.md) que usa o *parâmetro Handle* requer as permissões [UIPermissionWindow. @ Windows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , além das permissões exigidas pelo construtor que usa o parâmetro *attachedControl* .</span><span class="sxs-lookup"><span data-stu-id="0c5cc-104">The [**RealTimeStylus**](realtimestylus-class.md) that takes the *handle* parameter requires the [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) and [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) permissions, in addition to the permissions required by the constructor that takes the *attachedControl* parameter.</span></span>

<span data-ttu-id="0c5cc-105">Para obter mais informações sobre problemas de segurança e confiança, consulte [segurança e confiança](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="0c5cc-105">For more information about security and trust issues, see [Security and Trust](security-and-trust.md).</span></span>

 

 
