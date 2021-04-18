---
description: O design de SSPI permite que os SSPs adicionais sejam gravados e adicionados ao sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Gravando e instalando um provedor de suporte de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771824"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="7f8de-103">Gravando e instalando um provedor de suporte de segurança</span><span class="sxs-lookup"><span data-stu-id="7f8de-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="7f8de-104">O design de SSPI permite que os SSPs adicionais sejam gravados e adicionados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="7f8de-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="7f8de-105">Um [*SSP*](../secgloss/s-gly.md) específico de um modelo de segurança pode ser desenvolvido com a facilidade relativa ou uma grande complexidade, dependendo do nível de integração com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7f8de-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="7f8de-106">Um SSP de cliente que permite conexões com um novo tipo de servidor poderia ser desenvolvido muito rapidamente, enquanto que um SSP completo que fornece representação local exigiria mais esforço.</span><span class="sxs-lookup"><span data-stu-id="7f8de-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="7f8de-107">Os SSPs são instalados atualizando um valor de **\_ sz de reg** no registro, localizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7f8de-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="7f8de-108">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    </span><span class="sxs-lookup"><span data-stu-id="7f8de-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="7f8de-109">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="7f8de-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="7f8de-110">Uma única DLL pode conter vários SSPs.</span><span class="sxs-lookup"><span data-stu-id="7f8de-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f8de-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f8de-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f8de-112">Restrições sobre o registro e a instalação de um pacote de segurança</span><span class="sxs-lookup"><span data-stu-id="7f8de-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
