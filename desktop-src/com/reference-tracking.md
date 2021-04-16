---
title: Acompanhamento de referência
description: Acompanhamento de referência
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454363"
---
# <a name="reference-tracking"></a><span data-ttu-id="a85f5-103">Acompanhamento de referência</span><span class="sxs-lookup"><span data-stu-id="a85f5-103">Reference Tracking</span></span>

<span data-ttu-id="a85f5-104">O controle de referência pode impedir a liberação antecipada involuntária ou mal-intencionada de objetos.</span><span class="sxs-lookup"><span data-stu-id="a85f5-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="a85f5-105">Quando você habilita o acompanhamento de referência, está solicitando que as chamadas distribuídas do [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e do [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sejam autenticadas pelo com.</span><span class="sxs-lookup"><span data-stu-id="a85f5-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="a85f5-106">Quando o controle de referência está habilitado, o COM controla as contagens de referência por usuário para que um usuário possa chamar **Release** somente em objetos que o usuário chamou anteriormente no **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="a85f5-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="a85f5-107">Embora o controle de referência possa diminuir o desempenho, ele garante que, independentemente de quantas vezes um determinado usuário chamar a **versão**, os objetos e stubs ainda existirão se outra pessoa tiver uma referência a eles.</span><span class="sxs-lookup"><span data-stu-id="a85f5-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="a85f5-108">O cliente pode definir o acompanhamento de referência para um processo passando o \_ sinalizador de capacidade de REFS EOAC seguro \_ em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a85f5-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a85f5-109">Você também pode habilitar ou desabilitar o controle de referência para todos os aplicativos em um computador usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="a85f5-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="a85f5-110">Se o acompanhamento de referência estiver habilitado, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sempre usará as configurações de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="a85f5-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="a85f5-111">Nesse caso, as chamadas para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) em **IUnknown** falharão.</span><span class="sxs-lookup"><span data-stu-id="a85f5-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 