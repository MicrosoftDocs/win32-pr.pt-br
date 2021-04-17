---
title: Acesso remoto ao registro no Windows de 64 bits
description: O redirecionador de registro fornece acesso remoto ao registro em janelas de 64 bits por meio da função RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acesso remoto ao registro, programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790451"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="79436-104">Acesso remoto ao registro no Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="79436-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="79436-105">O redirecionador de registro fornece acesso remoto ao registro em janelas de 64 bits por meio da função [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .</span><span class="sxs-lookup"><span data-stu-id="79436-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="79436-106">Se o cliente for um aplicativo de 32 bits, ele acessará a exibição do registro padrão de 32 bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="79436-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="79436-107">Se o cliente for um aplicativo de 64 bits, ele acessará a exibição do registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="79436-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="79436-108">**Windows Server 2003:** Todos os clientes acessam a exibição de registro de 64 bits, a menos que o aplicativo use o \_ sinalizador 32KEY de WOW64 de chave \_ .</span><span class="sxs-lookup"><span data-stu-id="79436-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="79436-109">Esse comportamento mudou com o Windows Server 2003 com Service Pack 1 (SP1) e o Windows XP Professional x64 Edition, desde que o cliente e o servidor estejam executando essas versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="79436-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79436-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79436-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79436-111">Redirecionador de registro</span><span class="sxs-lookup"><span data-stu-id="79436-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="79436-112">Reflexão do registro</span><span class="sxs-lookup"><span data-stu-id="79436-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 