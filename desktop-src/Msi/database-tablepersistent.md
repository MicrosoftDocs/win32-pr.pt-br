---
description: A propriedade TablePersistent do objeto Database retorna o estado de persistência da tabela como um dos parâmetros a seguir.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propriedade Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778726"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="2157d-103">Propriedade Database. TablePersistent</span><span class="sxs-lookup"><span data-stu-id="2157d-103">Database.TablePersistent property</span></span>

<span data-ttu-id="2157d-104">A propriedade **TablePersistent** do objeto [**Database**](database-object.md) retorna o estado de persistência da tabela como um dos parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="2157d-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="2157d-105">Estado da tabela</span><span class="sxs-lookup"><span data-stu-id="2157d-105">Table state</span></span>               | <span data-ttu-id="2157d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="2157d-106">Value</span></span> | <span data-ttu-id="2157d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2157d-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="2157d-108">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="2157d-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="2157d-109">0</span><span class="sxs-lookup"><span data-stu-id="2157d-109">0</span></span>     | <span data-ttu-id="2157d-110">A tabela é temporária.</span><span class="sxs-lookup"><span data-stu-id="2157d-110">Table is temporary.</span></span>            |
| <span data-ttu-id="2157d-111">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="2157d-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="2157d-112">1</span><span class="sxs-lookup"><span data-stu-id="2157d-112">1</span></span>     | <span data-ttu-id="2157d-113">A tabela é persistente.</span><span class="sxs-lookup"><span data-stu-id="2157d-113">Table is persistent.</span></span>           |
| <span data-ttu-id="2157d-114">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="2157d-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="2157d-115">2</span><span class="sxs-lookup"><span data-stu-id="2157d-115">2</span></span>     | <span data-ttu-id="2157d-116">A tabela não está no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2157d-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="2157d-117">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="2157d-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="2157d-118">3</span><span class="sxs-lookup"><span data-stu-id="2157d-118">3</span></span>     | <span data-ttu-id="2157d-119">Nome de tabela inválido ou ausente.</span><span class="sxs-lookup"><span data-stu-id="2157d-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="2157d-120">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2157d-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2157d-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2157d-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="2157d-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2157d-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="2157d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2157d-123">Requirements</span></span>



| <span data-ttu-id="2157d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2157d-124">Requirement</span></span> | <span data-ttu-id="2157d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2157d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2157d-126">Versão</span><span class="sxs-lookup"><span data-stu-id="2157d-126">Version</span></span><br/> | <span data-ttu-id="2157d-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2157d-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2157d-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2157d-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2157d-129">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2157d-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2157d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2157d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="2157d-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2157d-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2157d-132">IID</span><span class="sxs-lookup"><span data-stu-id="2157d-132">IID</span></span><br/>     | <span data-ttu-id="2157d-133">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2157d-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




