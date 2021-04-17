---
description: Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Método __SystemSecurity:: Get9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749396"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="436c7-103">\_\_Método SystemSecurity:: Get9XUserList</span><span class="sxs-lookup"><span data-stu-id="436c7-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="436c7-104">O método [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="436c7-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="436c7-105">Isso funciona de forma semelhante ao descritor de segurança, mas é mais limitado.</span><span class="sxs-lookup"><span data-stu-id="436c7-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="436c7-106">Não há suporte para grupos e não há nenhum controle sobre o acesso local, pois o usuário local sempre tem acesso completo.</span><span class="sxs-lookup"><span data-stu-id="436c7-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="436c7-107">Tanto a negação quanto as entradas de controle de acesso (ACE) são permitidas e, por isso, a ordem de ACE é importante na DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="436c7-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="436c7-108">Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="436c7-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="436c7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="436c7-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="436c7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="436c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436c7-111">*UL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="436c7-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="436c7-112">Matriz de usuários.</span><span class="sxs-lookup"><span data-stu-id="436c7-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436c7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="436c7-113">Return value</span></span>

<span data-ttu-id="436c7-114">Esse método retorna um **HRESULT** que indica o status da chamada do método.</span><span class="sxs-lookup"><span data-stu-id="436c7-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="436c7-115">A lista a seguir lista os valores de retorno que são de significância a **Get9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="436c7-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="436c7-116">Para aplicativos de script e Visual Basic, o resultado pode ser [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="436c7-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="436c7-117">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="436c7-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="436c7-118">**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="436c7-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="436c7-119">Não há suporte para esse método em versões do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="436c7-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="436c7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="436c7-120">Requirements</span></span>



| <span data-ttu-id="436c7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="436c7-121">Requirement</span></span> | <span data-ttu-id="436c7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="436c7-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="436c7-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="436c7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="436c7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="436c7-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="436c7-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="436c7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="436c7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="436c7-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="436c7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="436c7-127">Namespace</span></span><br/>                | <span data-ttu-id="436c7-128">todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="436c7-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="436c7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="436c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436c7-130">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="436c7-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="436c7-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="436c7-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="436c7-132">**\_\_SystemSecurity:: Obtém-se**</span><span class="sxs-lookup"><span data-stu-id="436c7-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="436c7-133">**\_\_SystemSecurity:: definido**</span><span class="sxs-lookup"><span data-stu-id="436c7-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="436c7-134">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="436c7-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="436c7-135">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="436c7-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="436c7-136">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="436c7-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="436c7-137">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="436c7-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

