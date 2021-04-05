---
description: Pesquisa o executável especificado.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Função SdbGetMatchingExe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826355"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="880b5-103">Função SdbGetMatchingExe</span><span class="sxs-lookup"><span data-stu-id="880b5-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="880b5-104">Pesquisa o executável especificado.</span><span class="sxs-lookup"><span data-stu-id="880b5-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="880b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="880b5-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="880b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="880b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880b5-107">*hSDB* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="880b5-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-108">Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="880b5-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="880b5-109">*szPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="880b5-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-110">O caminho do executável.</span><span class="sxs-lookup"><span data-stu-id="880b5-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="880b5-111">*szModuleName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="880b5-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-112">O nome do módulo.</span><span class="sxs-lookup"><span data-stu-id="880b5-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="880b5-113">*pszEnvironment* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="880b5-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-114">As variáveis de ambiente a serem usadas como contexto de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="880b5-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="880b5-115">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="880b5-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-116">Esse parâmetro pode ser 0 ou **SDBGMEF \_ ignorar \_ ambiente** (0x1).</span><span class="sxs-lookup"><span data-stu-id="880b5-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="880b5-117">*pQueryResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="880b5-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="880b5-118">Uma estrutura [**SDBQUERYRESULT**](sdbqueryresult.md) .</span><span class="sxs-lookup"><span data-stu-id="880b5-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="880b5-119">Se nenhuma correspondência for encontrada, a estrutura conterá **TAGREF \_ nulo**.</span><span class="sxs-lookup"><span data-stu-id="880b5-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880b5-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="880b5-120">Return value</span></span>

<span data-ttu-id="880b5-121">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="880b5-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="880b5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="880b5-122">Remarks</span></span>

<span data-ttu-id="880b5-123">Quando você terminar com o [**TAGREF**](tagref.md)retornado, libere-o usando a função [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="880b5-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="880b5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="880b5-124">Requirements</span></span>



| <span data-ttu-id="880b5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="880b5-125">Requirement</span></span> | <span data-ttu-id="880b5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="880b5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="880b5-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="880b5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="880b5-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="880b5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="880b5-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="880b5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="880b5-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="880b5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="880b5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="880b5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="880b5-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="880b5-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="880b5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="880b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880b5-134">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="880b5-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="880b5-135">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="880b5-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




