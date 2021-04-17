---
description: A propriedade somente leitura databasetable do objeto de erro retorna o nome da tabela no banco de dados que causou o erro.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Error. Propriedade databasetable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752655"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="8556e-103">Erro. Propriedade databasetable</span><span class="sxs-lookup"><span data-stu-id="8556e-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="8556e-104">A propriedade somente leitura **databasetable** do objeto de [**erro**](error-object.md) retorna o nome da tabela no banco de dados que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="8556e-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="8556e-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8556e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8556e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8556e-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="8556e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8556e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="8556e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8556e-108">Remarks</span></span>

<span data-ttu-id="8556e-109">A coleção estará vazia se os valores não se aplicarem ao tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="8556e-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="8556e-110">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8556e-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="8556e-111">C++</span><span class="sxs-lookup"><span data-stu-id="8556e-111">C++</span></span>

<span data-ttu-id="8556e-112">Consulte [**obter a função \_ databasetable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .</span><span class="sxs-lookup"><span data-stu-id="8556e-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8556e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8556e-113">Requirements</span></span>



| <span data-ttu-id="8556e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8556e-114">Requirement</span></span> | <span data-ttu-id="8556e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8556e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8556e-116">Versão</span><span class="sxs-lookup"><span data-stu-id="8556e-116">Version</span></span><br/> | <span data-ttu-id="8556e-117">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8556e-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8556e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8556e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8556e-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="8556e-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8556e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8556e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="8556e-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8556e-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

