---
description: A \_ Propriedade Security do objeto SWbemObject é usada para ler ou definir as configurações de segurança para um objeto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297493"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="34628-103">Propriedade SWbemObject. Security \_</span><span class="sxs-lookup"><span data-stu-id="34628-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="34628-104">A **propriedade \_ Security** do objeto [**SWbemObject**](swbemobject.md) é usada para ler ou definir as configurações de segurança para um objeto **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="34628-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="34628-105">Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="34628-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="34628-106">As configurações de segurança nesse objeto não indicam as configurações de autenticação, representação ou privilégios feitas em uma conexão com Instrumentação de Gerenciamento do Windows (WMI) ou a segurança em vigor para o proxy quando um objeto é entregue a um coletor em uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="34628-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="34628-107">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="34628-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="34628-108">Definir a **propriedade \_ Security** de um objeto [**SWbemObject**](swbemobject.md) como **NULL** concede acesso ilimitado a todos o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="34628-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="34628-109">Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="34628-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="34628-110">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="34628-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="34628-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="34628-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34628-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34628-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="34628-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="34628-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="34628-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34628-114">Requirements</span></span>



| <span data-ttu-id="34628-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34628-115">Requirement</span></span> | <span data-ttu-id="34628-116">Valor</span><span class="sxs-lookup"><span data-stu-id="34628-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34628-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34628-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34628-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34628-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34628-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34628-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34628-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34628-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34628-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34628-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="34628-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34628-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="34628-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="34628-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="34628-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34628-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34628-125">DLL</span><span class="sxs-lookup"><span data-stu-id="34628-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34628-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34628-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34628-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="34628-127">CLSID</span></span><br/>                    | <span data-ttu-id="34628-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="34628-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="34628-129">IID</span><span class="sxs-lookup"><span data-stu-id="34628-129">IID</span></span><br/>                      | <span data-ttu-id="34628-130">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="34628-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="34628-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="34628-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34628-132">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="34628-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="34628-133">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="34628-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="34628-134">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="34628-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="34628-135">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="34628-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="34628-136">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="34628-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="34628-137">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="34628-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="34628-138">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="34628-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="34628-139">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="34628-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




