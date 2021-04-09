---
description: Estende a funcionalidade do SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objeto SWbemServicesEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091282"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="5aff3-103">Objeto SWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="5aff3-103">SWbemServicesEx object</span></span>

<span data-ttu-id="5aff3-104">O objeto **SWbemServicesEx** estende a funcionalidade de [**SWbemServices**](swbemservices.md).</span><span class="sxs-lookup"><span data-stu-id="5aff3-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="5aff3-105">Os métodos [**Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) permitem que uma classe ou uma instância seja salva em vários namespaces ou em um namespace diferente daquele em que uma instância foi criada.</span><span class="sxs-lookup"><span data-stu-id="5aff3-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="5aff3-106">Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5aff3-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="5aff3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5aff3-107">Members</span></span>

<span data-ttu-id="5aff3-108">O objeto **SWbemServicesEx** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5aff3-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="5aff3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5aff3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5aff3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5aff3-110">Methods</span></span>

<span data-ttu-id="5aff3-111">O objeto **SWbemServicesEx** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5aff3-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="5aff3-112">Método</span><span class="sxs-lookup"><span data-stu-id="5aff3-112">Method</span></span>                                       | <span data-ttu-id="5aff3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5aff3-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5aff3-114">**Posicione**</span><span class="sxs-lookup"><span data-stu-id="5aff3-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="5aff3-115">Salva o objeto no namespace associado ao objeto **SWbemServicesEx** e retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que contém o caminho do objeto no qual os dados foram gravados.</span><span class="sxs-lookup"><span data-stu-id="5aff3-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="5aff3-116">**PutAsync**</span><span class="sxs-lookup"><span data-stu-id="5aff3-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="5aff3-117">Salva um objeto de forma assíncrona em um namespace.</span><span class="sxs-lookup"><span data-stu-id="5aff3-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5aff3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5aff3-118">Remarks</span></span>

<span data-ttu-id="5aff3-119">Os métodos nessa classe podem ser chamados no modo semisynchronous ou no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="5aff3-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="5aff3-120">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5aff3-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aff3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aff3-121">Requirements</span></span>



| <span data-ttu-id="5aff3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aff3-122">Requirement</span></span> | <span data-ttu-id="5aff3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5aff3-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aff3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5aff3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5aff3-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aff3-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5aff3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5aff3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5aff3-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aff3-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aff3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5aff3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aff3-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aff3-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5aff3-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5aff3-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="5aff3-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5aff3-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5aff3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5aff3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aff3-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aff3-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5aff3-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="5aff3-134">CLSID</span></span><br/>                    | <span data-ttu-id="5aff3-135">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="5aff3-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="5aff3-136">IID</span><span class="sxs-lookup"><span data-stu-id="5aff3-136">IID</span></span><br/>                      | <span data-ttu-id="5aff3-137">ISWbemServicesEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="5aff3-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5aff3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5aff3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aff3-139">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="5aff3-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="5aff3-140">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="5aff3-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

