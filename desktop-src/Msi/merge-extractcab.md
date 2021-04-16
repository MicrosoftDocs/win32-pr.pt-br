---
description: O método ExtractCAB do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e o salva como o arquivo especificado. O instalador criará esse arquivo se ele ainda não existir e substituído se ele existir.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Método Merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758304"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="894d5-104">Método Merge. ExtractCAB</span><span class="sxs-lookup"><span data-stu-id="894d5-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="894d5-105">O método **ExtractCAB** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e o salva como o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="894d5-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="894d5-106">O instalador criará esse arquivo se ele ainda não existir e substituído se ele existir.</span><span class="sxs-lookup"><span data-stu-id="894d5-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="894d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="894d5-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="894d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="894d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894d5-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="894d5-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="894d5-110">O arquivo de destino totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="894d5-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="894d5-111">Return value</span></span>

<span data-ttu-id="894d5-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="894d5-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="894d5-113">C++</span><span class="sxs-lookup"><span data-stu-id="894d5-113">C++</span></span>

<span data-ttu-id="894d5-114">Consulte a função [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .</span><span class="sxs-lookup"><span data-stu-id="894d5-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="894d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="894d5-115">Requirements</span></span>



| <span data-ttu-id="894d5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="894d5-116">Requirement</span></span> | <span data-ttu-id="894d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="894d5-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="894d5-118">Versão</span><span class="sxs-lookup"><span data-stu-id="894d5-118">Version</span></span><br/> | <span data-ttu-id="894d5-119">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="894d5-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="894d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="894d5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="894d5-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="894d5-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="894d5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="894d5-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="894d5-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="894d5-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
