---
description: A propriedade Moduletable somente leitura retorna o nome da tabela no módulo que causou o erro.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Erro. Propriedade Moduletable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758782"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="53654-103">Erro. Propriedade Moduletable</span><span class="sxs-lookup"><span data-stu-id="53654-103">Error.ModuleTable property</span></span>

<span data-ttu-id="53654-104">A propriedade **moduletable** somente leitura retorna o nome da tabela no módulo que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="53654-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="53654-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="53654-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53654-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53654-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="53654-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="53654-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="53654-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="53654-108">Remarks</span></span>

<span data-ttu-id="53654-109">A coleção estará vazia se os valores não se aplicarem ao tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="53654-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="53654-110">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="53654-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="53654-111">C++</span><span class="sxs-lookup"><span data-stu-id="53654-111">C++</span></span>

<span data-ttu-id="53654-112">Consulte [**obter a função \_ moduletable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) .</span><span class="sxs-lookup"><span data-stu-id="53654-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="53654-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53654-113">Requirements</span></span>



| <span data-ttu-id="53654-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53654-114">Requirement</span></span> | <span data-ttu-id="53654-115">Valor</span><span class="sxs-lookup"><span data-stu-id="53654-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53654-116">Versão</span><span class="sxs-lookup"><span data-stu-id="53654-116">Version</span></span><br/> | <span data-ttu-id="53654-117">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="53654-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="53654-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53654-118">Header</span></span><br/>  | <dl> <span data-ttu-id="53654-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="53654-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="53654-120">DLL</span><span class="sxs-lookup"><span data-stu-id="53654-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="53654-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53654-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

