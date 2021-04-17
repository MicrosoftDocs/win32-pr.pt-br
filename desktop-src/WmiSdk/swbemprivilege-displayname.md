---
description: A propriedade DisplayName de um objeto SWbemPrivilege é uma cadeia de caracteres que exibe uma descrição de um objeto SWbemPrivilege.
ms.assetid: 9ed91a6a-e513-4a72-b8a9-3180e42b811f
ms.tgt_platform: multiple
title: Propriedade SWbemPrivilege. DisplayName (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.DisplayName
- ISWbemPrivilege.DisplayName
- ISWbemPrivilege.get_DisplayName
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bb45bdce52b1930f1893f7716d573033627e0cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797647"
---
# <a name="swbemprivilegedisplayname-property"></a><span data-ttu-id="d5725-103">Propriedade SWbemPrivilege. DisplayName</span><span class="sxs-lookup"><span data-stu-id="d5725-103">SWbemPrivilege.DisplayName property</span></span>

<span data-ttu-id="d5725-104">A propriedade **DisplayName** de um objeto [**SWbemPrivilege**](swbemprivilege.md) é uma cadeia de caracteres que exibe uma descrição de um objeto **SWbemPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d5725-104">The **DisplayName** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that displays a description of an **SWbemPrivilege** object.</span></span> <span data-ttu-id="d5725-105">Por exemplo, o privilégio que controla se um usuário pode executar o método de desligamento de um objeto tem a cadeia de caracteres "desligar o sistema" na propriedade **SWbemPrivilege. DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="d5725-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "Shut down the system" string in the **SWbemPrivilege.DisplayName** property.</span></span> <span data-ttu-id="d5725-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d5725-106">This property is read-only.</span></span>

<span data-ttu-id="d5725-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d5725-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d5725-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d5725-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5725-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5725-109">Syntax</span></span>


```VB
SWbemPrivilege.DisplayName As 
```



## <a name="property-value"></a><span data-ttu-id="d5725-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d5725-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="d5725-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5725-111">Requirements</span></span>



| <span data-ttu-id="d5725-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5725-112">Requirement</span></span> | <span data-ttu-id="d5725-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d5725-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5725-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5725-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d5725-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5725-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5725-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5725-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d5725-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5725-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5725-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5725-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5725-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5725-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5725-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d5725-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5725-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d5725-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d5725-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d5725-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5725-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5725-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5725-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="d5725-124">CLSID</span></span><br/>                    | <span data-ttu-id="d5725-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="d5725-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="d5725-126">IID</span><span class="sxs-lookup"><span data-stu-id="d5725-126">IID</span></span><br/>                      | <span data-ttu-id="d5725-127">ISWbemPrivilege de IID \_</span><span class="sxs-lookup"><span data-stu-id="d5725-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




