---
description: A propriedade Name de um objeto SWbemPrivilege é uma cadeia de caracteres que descreve exclusivamente um privilégio.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Propriedade SWbemPrivilege.Name (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171781"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="e3d1a-103">Propriedade SWbemPrivilege.Name</span><span class="sxs-lookup"><span data-stu-id="e3d1a-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="e3d1a-104">A propriedade **Name** de um objeto [**SWbemPrivilege**](swbemprivilege.md) é uma cadeia de caracteres que descreve exclusivamente um privilégio.</span><span class="sxs-lookup"><span data-stu-id="e3d1a-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="e3d1a-105">Por exemplo, o privilégio que controla se um usuário pode executar o método de desligamento de um objeto tem a cadeia de caracteres "SeShutdownPrivilege" na propriedade **SWbemPrivilege.Name** .</span><span class="sxs-lookup"><span data-stu-id="e3d1a-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="e3d1a-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e3d1a-106">This property is read-only.</span></span>

<span data-ttu-id="e3d1a-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e3d1a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e3d1a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e3d1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d1a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3d1a-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="e3d1a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e3d1a-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d1a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3d1a-111">Requirements</span></span>



| <span data-ttu-id="e3d1a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d1a-112">Requirement</span></span> | <span data-ttu-id="e3d1a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e3d1a-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d1a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3d1a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d1a-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3d1a-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3d1a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3d1a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d1a-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3d1a-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3d1a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3d1a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d1a-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d1a-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3d1a-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e3d1a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3d1a-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3d1a-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3d1a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e3d1a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3d1a-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3d1a-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3d1a-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="e3d1a-124">CLSID</span></span><br/>                    | <span data-ttu-id="e3d1a-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="e3d1a-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="e3d1a-126">IID</span><span class="sxs-lookup"><span data-stu-id="e3d1a-126">IID</span></span><br/>                      | <span data-ttu-id="e3d1a-127">ISWbemPrivilege de IID \_</span><span class="sxs-lookup"><span data-stu-id="e3d1a-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




