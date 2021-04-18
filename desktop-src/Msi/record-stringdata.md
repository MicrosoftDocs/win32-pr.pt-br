---
description: A propriedade StringData do objeto Record é uma propriedade de leitura/gravação que transfere dados de cadeia de caracteres para dentro ou para fora de um campo especificado no registro. Se um inteiro ou um objeto tiver sido armazenado, seu valor de cadeia de caracteres será retornado.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Propriedade Record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756722"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="5d225-104">Propriedade Record. StringData</span><span class="sxs-lookup"><span data-stu-id="5d225-104">Record.StringData property</span></span>

<span data-ttu-id="5d225-105">A propriedade **StringData** do objeto [**Record**](record-object.md) é uma propriedade de leitura/gravação que transfere dados de cadeia de caracteres para dentro ou para fora de um campo especificado no registro.</span><span class="sxs-lookup"><span data-stu-id="5d225-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="5d225-106">Se um inteiro ou um objeto tiver sido armazenado, seu valor de cadeia de caracteres será retornado.</span><span class="sxs-lookup"><span data-stu-id="5d225-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="5d225-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5d225-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d225-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d225-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5d225-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5d225-109">Property value</span></span>

<span data-ttu-id="5d225-110">Campo obrigatório número do valor dentro do registro, baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="5d225-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d225-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d225-111">Remarks</span></span>

<span data-ttu-id="5d225-112">O valor retornado de um campo inexistente é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5d225-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="5d225-113">Para definir um campo de cadeia de caracteres de registro como nulo, use uma variante vazia ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5d225-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="5d225-114">A tentativa de armazenar um valor em um campo inexistente causa um erro.</span><span class="sxs-lookup"><span data-stu-id="5d225-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d225-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d225-115">Requirements</span></span>



| <span data-ttu-id="5d225-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d225-116">Requirement</span></span> | <span data-ttu-id="5d225-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d225-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d225-118">Versão</span><span class="sxs-lookup"><span data-stu-id="5d225-118">Version</span></span><br/> | <span data-ttu-id="5d225-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d225-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d225-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d225-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d225-121">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d225-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5d225-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5d225-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d225-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d225-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5d225-124">IID</span><span class="sxs-lookup"><span data-stu-id="5d225-124">IID</span></span><br/>     | <span data-ttu-id="5d225-125">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d225-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




