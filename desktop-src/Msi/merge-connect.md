---
description: O método Connect do objeto de mesclagem conecta um módulo a um recurso adicional. O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados. O recurso deve existir antes de chamar essa função.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Método Merge. Connect (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757120"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="d462e-105">Método Merge. Connect</span><span class="sxs-lookup"><span data-stu-id="d462e-105">Merge.Connect method</span></span>

<span data-ttu-id="d462e-106">O método **Connect** do objeto de [**mesclagem**](merge-object.md) conecta um módulo a um recurso adicional.</span><span class="sxs-lookup"><span data-stu-id="d462e-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="d462e-107">O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d462e-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="d462e-108">O recurso deve existir antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="d462e-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="d462e-109">As alterações feitas no banco de dados não são salvas no disco, a menos que o método [**CloseDatabase**](merge-closedatabase.md) seja chamado com *BCommit* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="d462e-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d462e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d462e-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="d462e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d462e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d462e-112">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="d462e-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d462e-113">O nome de um recurso já existente no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d462e-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d462e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d462e-114">Return value</span></span>

<span data-ttu-id="d462e-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d462e-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d462e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d462e-116">Remarks</span></span>

<span data-ttu-id="d462e-117">Os erros podem ser recuperados por meio da propriedade [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="d462e-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="d462e-118">Erros e mensagens informativas são postados no arquivo de log atual.</span><span class="sxs-lookup"><span data-stu-id="d462e-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="d462e-119">C++</span><span class="sxs-lookup"><span data-stu-id="d462e-119">C++</span></span>

<span data-ttu-id="d462e-120">Consulte [**conectar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) função.</span><span class="sxs-lookup"><span data-stu-id="d462e-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d462e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d462e-121">Requirements</span></span>



| <span data-ttu-id="d462e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d462e-122">Requirement</span></span> | <span data-ttu-id="d462e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d462e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d462e-124">Versão</span><span class="sxs-lookup"><span data-stu-id="d462e-124">Version</span></span><br/> | <span data-ttu-id="d462e-125">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d462e-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d462e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d462e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d462e-127"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d462e-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d462e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d462e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d462e-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d462e-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
