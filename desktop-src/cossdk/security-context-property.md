---
description: Propriedade de contexto de segurança
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propriedade de contexto de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164156"
---
# <a name="security-context-property"></a><span data-ttu-id="ee95a-103">Propriedade de contexto de segurança</span><span class="sxs-lookup"><span data-stu-id="ee95a-103">Security Context Property</span></span>

<span data-ttu-id="ee95a-104">Assim como ocorre com cada serviço automático fornecido pelo COM+, a verificação automática de função baseia-se nas propriedades incluídas no contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="ee95a-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="ee95a-105">A determinação de se uma verificação de segurança deve ser executada em uma chamada em um componente é baseada na propriedade de segurança no contexto de objeto criado quando o componente configurado é instanciado.</span><span class="sxs-lookup"><span data-stu-id="ee95a-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="ee95a-106">Geralmente, você não precisa se preocupar com essa propriedade; Ele é usado diretamente pelo COM+, não por você.</span><span class="sxs-lookup"><span data-stu-id="ee95a-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="ee95a-107">No entanto, em algumas circunstâncias, talvez você queira um controle estrito sobre a ativação de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ee95a-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="ee95a-108">Nesse caso, a propriedade de segurança pode afetar em qual contexto seu objeto é ativado.</span><span class="sxs-lookup"><span data-stu-id="ee95a-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="ee95a-109">Ou seja, se um objeto tiver uma configuração incompatível com o contexto de seu criador, ele será ativado em seu próprio contexto.</span><span class="sxs-lookup"><span data-stu-id="ee95a-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="ee95a-110">A propriedade de segurança pode influenciar isso, assim como qualquer propriedade no contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="ee95a-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="ee95a-111">Se não quiser que as configurações de segurança influenciem a ativação, você poderá escolher somente a verificação de acesso no nível de processo.</span><span class="sxs-lookup"><span data-stu-id="ee95a-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="ee95a-112">Isso suprime a propriedade Security no contexto do objeto, embora efetivamente desabilite a verificação baseada em função e torne [as informações de contexto de chamada de segurança](security-call-context-information.md) indisponíveis.</span><span class="sxs-lookup"><span data-stu-id="ee95a-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="ee95a-113">Para obter mais informações sobre verificações de acesso no nível do processo, consulte [limites de segurança](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="ee95a-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="ee95a-114">Para ver como definir a segurança em nível de processo, consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ee95a-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="ee95a-115">Para obter mais informações sobre o contexto de objeto, consulte [contextos](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="ee95a-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee95a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee95a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee95a-117">Criando funções com eficiência</span><span class="sxs-lookup"><span data-stu-id="ee95a-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="ee95a-118">Limites de segurança</span><span class="sxs-lookup"><span data-stu-id="ee95a-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="ee95a-119">Informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="ee95a-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="ee95a-120">Usando funções para autorização de cliente</span><span class="sxs-lookup"><span data-stu-id="ee95a-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



