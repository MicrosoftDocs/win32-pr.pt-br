---
title: Persistência de configuração
description: Persistência de configuração
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- SDK do Windows Media Format, persistência
- SDK do Windows Media Format, persistência de configuração
- ASF (Advanced Systems Format), persistência
- ASF (formato de sistemas avançados), persistência
- ASF (Advanced Systems Format), persistência de configuração
- ASF (formato de sistemas avançados), persistência de configuração
- persistência de configuração
- persistência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365619"
---
# <a name="configuration-persistence"></a><span data-ttu-id="28545-111">Persistência de configuração</span><span class="sxs-lookup"><span data-stu-id="28545-111">Configuration Persistence</span></span>

<span data-ttu-id="28545-112">Nenhuma das propriedades habilitadas para gravação descritas nesta documentação é salva pelo SDK do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="28545-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="28545-113">Cada aplicativo que usa o SDK deve fornecer seus próprios procedimentos de persistência, conforme necessário, e invocar o método Set apropriado em cada instância do SDK.</span><span class="sxs-lookup"><span data-stu-id="28545-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="28545-114">Dessa forma, as alterações de configuração feitas por um aplicativo não afetam outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28545-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="28545-115">Por exemplo, alterar o tempo de buffer em um player não afeta outro jogador.</span><span class="sxs-lookup"><span data-stu-id="28545-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="28545-116">A única exceção a essa regra é para as informações de credenciais.</span><span class="sxs-lookup"><span data-stu-id="28545-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="28545-117">Se o aplicativo indicar, em seu retorno, da chamada **AcquireCredentials** , que as informações de ID de usuário e senha devem ser mantidas, o SDK salvará essas informações.</span><span class="sxs-lookup"><span data-stu-id="28545-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28545-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28545-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28545-119">**Implementando a funcionalidade de rede**</span><span class="sxs-lookup"><span data-stu-id="28545-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="28545-120">**Interface IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="28545-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




