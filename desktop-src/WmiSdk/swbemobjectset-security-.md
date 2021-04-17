---
description: A \_ Propriedade Security do objeto SWbemObjectSet é usada para obter ou definir as configurações de segurança para um objeto SWbemObjectSet. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Propriedade SWbemObjectSet.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762322"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="e76ae-104">Propriedade SWbemObjectSet. Security \_</span><span class="sxs-lookup"><span data-stu-id="e76ae-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="e76ae-105">A **propriedade \_ Security** do objeto [**SWbemObjectSet**](swbemobjectset.md) é usada para obter ou definir as configurações de segurança para um objeto **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="e76ae-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="e76ae-106">Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="e76ae-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="e76ae-107">Definir a [**propriedade \_ Security**](swbemobject-security-.md) de um objeto [**SWbemObjectSet**](swbemobjectset.md) como **NULL** concede acesso ilimitado a todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="e76ae-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="e76ae-108">Para obter mais informações sobre as implicações de acesso ilimitado, consulte [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="e76ae-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="e76ae-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e76ae-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e76ae-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e76ae-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76ae-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e76ae-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="e76ae-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e76ae-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e76ae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76ae-113">Requirements</span></span>



| <span data-ttu-id="e76ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76ae-114">Requirement</span></span> | <span data-ttu-id="e76ae-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e76ae-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e76ae-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e76ae-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e76ae-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e76ae-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e76ae-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e76ae-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e76ae-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e76ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76ae-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76ae-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e76ae-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e76ae-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e76ae-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e76ae-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e76ae-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e76ae-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e76ae-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e76ae-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e76ae-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="e76ae-126">CLSID</span></span><br/>                    | <span data-ttu-id="e76ae-127">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="e76ae-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="e76ae-128">IID</span><span class="sxs-lookup"><span data-stu-id="e76ae-128">IID</span></span><br/>                      | <span data-ttu-id="e76ae-129">ISWbemObjectSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="e76ae-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="e76ae-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e76ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76ae-131">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="e76ae-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="e76ae-132">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="e76ae-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="e76ae-133">Protegendo clientes de script</span><span class="sxs-lookup"><span data-stu-id="e76ae-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




