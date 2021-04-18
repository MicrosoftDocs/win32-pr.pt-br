---
title: Definindo Process-Wide segurança
description: Há várias maneiras de definir a segurança de todo o processo.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105768220"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="d1f41-103">Definindo Process-Wide segurança</span><span class="sxs-lookup"><span data-stu-id="d1f41-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="d1f41-104">Há várias maneiras de definir a segurança de todo o processo.</span><span class="sxs-lookup"><span data-stu-id="d1f41-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="d1f41-105">A primeira maneira, usando a ferramenta Dcomcnfg.exe, é mais fácil porque não requer programação.</span><span class="sxs-lookup"><span data-stu-id="d1f41-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="d1f41-106">A segunda técnica oferece ao programador mais controle e requer uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d1f41-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d1f41-107">Outra técnica é definir a segurança de todo o processo no registro usando a chave [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f41-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="d1f41-108">Para obter mais informações sobre essas técnicas, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d1f41-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="d1f41-109">Definindo Process-Wide segurança usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="d1f41-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="d1f41-110">Definindo Process-Wide segurança com CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="d1f41-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="d1f41-111">Configurando a segurança do Process-Wide por meio do registro</span><span class="sxs-lookup"><span data-stu-id="d1f41-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="d1f41-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1f41-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1f41-113">Definindo a segurança no nível de proxy da interface</span><span class="sxs-lookup"><span data-stu-id="d1f41-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="d1f41-114">Definindo a segurança para aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="d1f41-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




