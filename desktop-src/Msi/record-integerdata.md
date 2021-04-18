---
description: Essa é a propriedade IntegerData do objeto Record. Essa propriedade de leitura/gravação transfere dados inteiros de 32 bits para dentro ou para fora de um campo especificado no registro. Se um valor de campo não puder ser convertido em um inteiro, msiDatabaseNullInteger será retornado.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Propriedade Record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748572"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="c5853-105">Propriedade Record. IntegerData</span><span class="sxs-lookup"><span data-stu-id="c5853-105">Record.IntegerData property</span></span>

<span data-ttu-id="c5853-106">Essa é a propriedade **IntegerData** do objeto [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c5853-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="c5853-107">Essa propriedade de leitura/gravação transfere dados inteiros de 32 bits para dentro ou para fora de um campo especificado no registro.</span><span class="sxs-lookup"><span data-stu-id="c5853-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="c5853-108">Se um valor de campo não puder ser convertido em um inteiro, msiDatabaseNullInteger será retornado.</span><span class="sxs-lookup"><span data-stu-id="c5853-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="c5853-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c5853-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5853-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5853-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="c5853-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c5853-111">Property value</span></span>

<span data-ttu-id="c5853-112">Campo obrigatório número do valor dentro do registro, baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="c5853-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5853-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5853-113">Remarks</span></span>

<span data-ttu-id="c5853-114">Para definir um campo de inteiro de registro como nulo, use msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="c5853-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="c5853-115">O valor retornado de um campo inexistente é msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="c5853-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="c5853-116">A tentativa de armazenar um valor em um campo inexistente causa um erro.</span><span class="sxs-lookup"><span data-stu-id="c5853-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5853-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5853-117">Requirements</span></span>



| <span data-ttu-id="c5853-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5853-118">Requirement</span></span> | <span data-ttu-id="c5853-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c5853-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5853-120">Versão</span><span class="sxs-lookup"><span data-stu-id="c5853-120">Version</span></span><br/> | <span data-ttu-id="c5853-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5853-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5853-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5853-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5853-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5853-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c5853-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c5853-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5853-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5853-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c5853-126">IID</span><span class="sxs-lookup"><span data-stu-id="c5853-126">IID</span></span><br/>     | <span data-ttu-id="c5853-127">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c5853-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




