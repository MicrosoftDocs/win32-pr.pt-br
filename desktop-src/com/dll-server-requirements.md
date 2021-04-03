---
title: Requisitos do servidor DLL
description: Embora a maioria das DLLs possa ser executada em um substituto, algumas DLLs não podem.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006172"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="d65bc-103">Requisitos do servidor DLL</span><span class="sxs-lookup"><span data-stu-id="d65bc-103">DLL Server Requirements</span></span>

<span data-ttu-id="d65bc-104">Embora a maioria das DLLs possa ser executada em um substituto, algumas DLLs não podem.</span><span class="sxs-lookup"><span data-stu-id="d65bc-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="d65bc-105">O dll deve estar bem se comparado se você quiser usar o substituto fornecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d65bc-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="d65bc-106">Por exemplo, uma DLL que chama métodos que registram retornos de chamada do cliente tentaria invocar esses retornos de chamada como se os ponteiros de função recebidos fossem instruções em seu espaço de endereço, o que não é o caso.</span><span class="sxs-lookup"><span data-stu-id="d65bc-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="d65bc-107">Da mesma forma, uma DLL que usa uma variável global que espera que o cliente acesse não funcionaria.</span><span class="sxs-lookup"><span data-stu-id="d65bc-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="d65bc-108">Em geral, os parâmetros que não podem ser corretamente empacotados impedirão que o servidor DLL seja executado fora do processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="d65bc-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="d65bc-109">Em muitos casos, você pode escrever um substituto personalizado especificamente projetado para compensar o comportamento "inadequado".</span><span class="sxs-lookup"><span data-stu-id="d65bc-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="d65bc-110">(Para obter mais informações, consulte [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).)</span><span class="sxs-lookup"><span data-stu-id="d65bc-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="d65bc-111">Se o servidor DLL usar interfaces personalizadas, você precisará garantir que o código de marshaling esteja disponível para essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d65bc-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="d65bc-112">Por exemplo, você pode criar e registrar uma DLL de proxy ou fornecer e registrar uma biblioteca de tipos que permitiria que o servidor funcionasse corretamente durante a execução em um substituto.</span><span class="sxs-lookup"><span data-stu-id="d65bc-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="d65bc-113">Os servidores DLL serão carregados somente em um processo substituto em execução no contexto de segurança adequado.</span><span class="sxs-lookup"><span data-stu-id="d65bc-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="d65bc-114">O contexto de segurança para o substituto do servidor DLL é determinado da mesma maneira que para servidores EXE.</span><span class="sxs-lookup"><span data-stu-id="d65bc-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="d65bc-115">O substituto do servidor DLL é executado no mesmo contexto de segurança que o cliente, a menos que um valor **runas** , que determina o contexto de segurança, seja definido na seção do registro [AppID](appid-clsid.md) do servidor.</span><span class="sxs-lookup"><span data-stu-id="d65bc-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d65bc-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d65bc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65bc-117">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="d65bc-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




