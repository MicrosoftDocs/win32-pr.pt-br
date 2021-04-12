---
description: A propriedade Security do objeto SWbemObjectPath é usada para obter ou definir os componentes de segurança de um caminho de objeto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165194"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="b27ab-103">Propriedade SWbemObjectPath. Security \_</span><span class="sxs-lookup"><span data-stu-id="b27ab-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="b27ab-104">A propriedade **Security** do objeto [**SWbemObjectPath**](swbemobjectpath.md) é usada para obter ou definir os componentes de segurança de um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="b27ab-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="b27ab-105">Observe que ele não é usado para definir atributos de segurança do objeto **SWbemObjectPath** em si.</span><span class="sxs-lookup"><span data-stu-id="b27ab-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="b27ab-106">Ele é usado apenas para representar os componentes de segurança do caminho para um objeto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b27ab-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="b27ab-107">Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="b27ab-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="b27ab-108">Definir a [**propriedade \_ Security**](swbemobject-security-.md) de um objeto [**SWbemObjectPath**](swbemobjectset.md) como **NULL** concede acesso ilimitado a todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="b27ab-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="b27ab-109">Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="b27ab-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="b27ab-110">Para obter mais informações, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b27ab-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b27ab-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b27ab-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27ab-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b27ab-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="b27ab-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b27ab-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="b27ab-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b27ab-114">Requirements</span></span>



| <span data-ttu-id="b27ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27ab-115">Requirement</span></span> | <span data-ttu-id="b27ab-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b27ab-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b27ab-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b27ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b27ab-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b27ab-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b27ab-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b27ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b27ab-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b27ab-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b27ab-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b27ab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27ab-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27ab-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b27ab-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b27ab-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b27ab-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b27ab-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b27ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b27ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b27ab-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b27ab-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b27ab-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="b27ab-127">CLSID</span></span><br/>                    | <span data-ttu-id="b27ab-128">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="b27ab-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="b27ab-129">IID</span><span class="sxs-lookup"><span data-stu-id="b27ab-129">IID</span></span><br/>                      | <span data-ttu-id="b27ab-130">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="b27ab-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="b27ab-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b27ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27ab-132">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="b27ab-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="b27ab-133">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="b27ab-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="b27ab-134">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="b27ab-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




