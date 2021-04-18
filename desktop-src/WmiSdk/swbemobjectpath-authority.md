---
description: A propriedade Authority do objeto SWbemObjectPath contém uma cadeia de caracteres que define o componente de autoridade do caminho do objeto.
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Authority (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793902"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="504ef-103">Propriedade SWbemObjectPath. Authority</span><span class="sxs-lookup"><span data-stu-id="504ef-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="504ef-104">A propriedade **Authority** do objeto [**SWbemObjectPath**](swbemobjectpath.md) contém uma cadeia de caracteres que define o componente de autoridade do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="504ef-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="504ef-105">Para obter mais informações, consulte o parâmetro *strAuthority* do método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="504ef-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="504ef-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="504ef-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="504ef-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="504ef-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="504ef-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="504ef-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="504ef-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="504ef-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="504ef-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="504ef-110">Requirements</span></span>



| <span data-ttu-id="504ef-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="504ef-111">Requirement</span></span> | <span data-ttu-id="504ef-112">Valor</span><span class="sxs-lookup"><span data-stu-id="504ef-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="504ef-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="504ef-113">Minimum supported client</span></span><br/> | <span data-ttu-id="504ef-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="504ef-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="504ef-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="504ef-115">Minimum supported server</span></span><br/> | <span data-ttu-id="504ef-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="504ef-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="504ef-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="504ef-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="504ef-118"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="504ef-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="504ef-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="504ef-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="504ef-120"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="504ef-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="504ef-121">DLL</span><span class="sxs-lookup"><span data-stu-id="504ef-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="504ef-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="504ef-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="504ef-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="504ef-123">CLSID</span></span><br/>                    | <span data-ttu-id="504ef-124">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="504ef-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="504ef-125">IID</span><span class="sxs-lookup"><span data-stu-id="504ef-125">IID</span></span><br/>                      | <span data-ttu-id="504ef-126">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="504ef-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




