---
title: Provedor WMI de Serviços de Área de Trabalho Remota
description: O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, provedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007711"
---
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="17068-104">Provedor WMI de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="17068-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="17068-105">O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.</span><span class="sxs-lookup"><span data-stu-id="17068-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="17068-106">A DLL do provedor é carregada pelo processo de gerenciamento do Windows (Winmgmt.exe) quando um cliente faz uma solicitação ao servidor.</span><span class="sxs-lookup"><span data-stu-id="17068-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="17068-107">A administração é possível usando os métodos de provedor.</span><span class="sxs-lookup"><span data-stu-id="17068-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="17068-108">O provedor é registrado como uma instância e um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="17068-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="17068-109">O provedor WMI Serviços de Área de Trabalho Remota foi implementado como um provedor dinâmico derivado da classe base [**de \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) , herdando todas as suas propriedades e métodos e uma biblioteca de vínculo dinâmico em processo.</span><span class="sxs-lookup"><span data-stu-id="17068-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="17068-110">Para obter mais informações, consulte a [referência do provedor WMI serviços de área de trabalho remota](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="17068-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17068-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17068-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17068-112">Serviços de Área de Trabalho Remota referência do provedor WMI</span><span class="sxs-lookup"><span data-stu-id="17068-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 