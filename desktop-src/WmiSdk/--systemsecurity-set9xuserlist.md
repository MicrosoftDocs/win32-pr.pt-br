---
description: Define os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: 'Método __SystemSecurity:: Set9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813325"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="91925-103">\_\_Método SystemSecurity:: Set9XUserList</span><span class="sxs-lookup"><span data-stu-id="91925-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="91925-104">O método **\_ \_ SystemSecurity:: Set9XUserList** define os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="91925-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="91925-105">A lista é especificada como uma matriz de objetos inseridos onde cada objeto é uma instância da classe [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) .</span><span class="sxs-lookup"><span data-stu-id="91925-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="91925-106">Isso funciona de forma semelhante ao descritor de segurança, mas é mais limitado.</span><span class="sxs-lookup"><span data-stu-id="91925-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="91925-107">Não há suporte para grupos e não há nenhum controle sobre o acesso local, pois o usuário local sempre tem acesso completo.</span><span class="sxs-lookup"><span data-stu-id="91925-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="91925-108">Tanto a negação quanto as entradas de controle de acesso (ACE) são permitidas e, por isso, a ordem de ACE é importante na DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="91925-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="91925-109">Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="91925-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="91925-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91925-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="91925-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91925-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91925-112">*UL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91925-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91925-113">Matriz de usuários.</span><span class="sxs-lookup"><span data-stu-id="91925-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91925-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91925-114">Return value</span></span>

<span data-ttu-id="91925-115">Esse método retorna um **HRESULT** que indica o status da chamada do método.</span><span class="sxs-lookup"><span data-stu-id="91925-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="91925-116">A lista a seguir lista os valores de retorno que são de significância a **Set9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="91925-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="91925-117">Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="91925-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="91925-118">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="91925-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="91925-119">**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="91925-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="91925-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="91925-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91925-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91925-121">Requirements</span></span>



| <span data-ttu-id="91925-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="91925-122">Requirement</span></span> | <span data-ttu-id="91925-123">Valor</span><span class="sxs-lookup"><span data-stu-id="91925-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="91925-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91925-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91925-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91925-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="91925-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91925-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91925-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91925-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="91925-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="91925-128">Namespace</span></span><br/>                | <span data-ttu-id="91925-129">todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="91925-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="91925-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="91925-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91925-131">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="91925-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="91925-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="91925-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="91925-133">**\_\_SystemSecurity:: Obtém-se**</span><span class="sxs-lookup"><span data-stu-id="91925-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="91925-134">**\_\_SystemSecurity:: definido**</span><span class="sxs-lookup"><span data-stu-id="91925-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="91925-135">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="91925-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="91925-136">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="91925-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="91925-137">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="91925-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="91925-138">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="91925-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

