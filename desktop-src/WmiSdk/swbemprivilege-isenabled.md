---
description: A propriedade IsEnabled de um objeto SWbemPrivilege é um valor booliano que você usa para habilitar ou desabilitar esse privilégio. Para obter mais informações sobre as consequências de habilitar privilégios específicos, consulte executando com privilégios especiais.
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: Propriedade SWbemPrivilege. IsEnabled (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793207"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="b1500-104">Propriedade SWbemPrivilege. IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b1500-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="b1500-105">A propriedade **IsEnabled** de um objeto [**SWbemPrivilege**](swbemprivilege.md) é um valor booliano que você usa para habilitar ou desabilitar esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="b1500-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="b1500-106">Para obter mais informações sobre as consequências de habilitar privilégios específicos, consulte [**executando com privilégios especiais**](swbemsecurity-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="b1500-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="b1500-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b1500-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b1500-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b1500-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1500-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1500-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b1500-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b1500-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="b1500-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1500-111">Requirements</span></span>



| <span data-ttu-id="b1500-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1500-112">Requirement</span></span> | <span data-ttu-id="b1500-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b1500-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1500-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1500-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b1500-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1500-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1500-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1500-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b1500-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1500-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1500-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1500-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1500-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1500-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1500-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b1500-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1500-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1500-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1500-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1500-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1500-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1500-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1500-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1500-124">CLSID</span></span><br/>                    | <span data-ttu-id="b1500-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="b1500-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="b1500-126">IID</span><span class="sxs-lookup"><span data-stu-id="b1500-126">IID</span></span><br/>                      | <span data-ttu-id="b1500-127">ISWbemPrivilege de IID \_</span><span class="sxs-lookup"><span data-stu-id="b1500-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




