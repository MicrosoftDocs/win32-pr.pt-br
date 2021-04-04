---
description: A \_ Propriedade Security do objeto SWbemLocator é usada para ler ou definir as configurações de segurança para um objeto SWbemLocator. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Propriedade SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661763"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="2874f-104">Propriedade SWbemLocator. Security \_</span><span class="sxs-lookup"><span data-stu-id="2874f-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="2874f-105">A **propriedade \_ Security** do objeto [**SWbemLocator**](swbemlocator.md) é usada para ler ou definir as configurações de segurança para um objeto **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="2874f-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="2874f-106">Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="2874f-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="2874f-107">Definir a **propriedade \_ Security** de um objeto [**SWbemLocator**](swbemlocator.md) como **NULL** concede acesso ilimitado a todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="2874f-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="2874f-108">Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="2874f-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="2874f-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2874f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2874f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2874f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2874f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2874f-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="2874f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2874f-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2874f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2874f-113">Remarks</span></span>

<span data-ttu-id="2874f-114">As propriedades de um objeto **SWbemLocator. \_ Security** não têm valores padrão.</span><span class="sxs-lookup"><span data-stu-id="2874f-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="2874f-115">Se você tentar obter o valor de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) em um objeto [**SWbemLocator**](swbemlocator.md) antes de defini-lo, ocorrerá um erro de [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .</span><span class="sxs-lookup"><span data-stu-id="2874f-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="2874f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2874f-116">Requirements</span></span>



| <span data-ttu-id="2874f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2874f-117">Requirement</span></span> | <span data-ttu-id="2874f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2874f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2874f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2874f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2874f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2874f-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2874f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2874f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2874f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2874f-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2874f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2874f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2874f-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2874f-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2874f-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2874f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2874f-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2874f-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2874f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2874f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2874f-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2874f-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2874f-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="2874f-129">CLSID</span></span><br/>                    | <span data-ttu-id="2874f-130">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="2874f-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="2874f-131">IID</span><span class="sxs-lookup"><span data-stu-id="2874f-131">IID</span></span><br/>                      | <span data-ttu-id="2874f-132">ISWbemLocator de IID \_</span><span class="sxs-lookup"><span data-stu-id="2874f-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="2874f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2874f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2874f-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="2874f-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="2874f-135">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="2874f-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="2874f-136">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="2874f-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="2874f-137">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="2874f-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="2874f-138">**Objeto SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="2874f-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="2874f-139">Protegendo uma conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="2874f-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




