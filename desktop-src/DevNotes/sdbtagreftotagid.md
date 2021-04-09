---
description: Recupera o TAGID e um identificador para o banco de dados de Shim para o TAGREF especificado.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Função SdbTagRefToTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089067"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="da1d3-103">Função SdbTagRefToTagID</span><span class="sxs-lookup"><span data-stu-id="da1d3-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="da1d3-104">Recupera o **TagId** e um identificador para o banco de dados de Shim para o [**TAGREF**](tagref.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="da1d3-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da1d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da1d3-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="da1d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da1d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1d3-107">*hSDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d3-108">Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="da1d3-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="da1d3-109">*trWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d3-110">O [**TAGREF**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="da1d3-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="da1d3-111">*ppdb* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d3-112">O identificador resultante para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="da1d3-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="da1d3-113">*ptiWhich* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d3-114">O **TagId** resultante.</span><span class="sxs-lookup"><span data-stu-id="da1d3-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1d3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da1d3-115">Return value</span></span>

<span data-ttu-id="da1d3-116">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="da1d3-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1d3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1d3-117">Requirements</span></span>



| <span data-ttu-id="da1d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1d3-118">Requirement</span></span> | <span data-ttu-id="da1d3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="da1d3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da1d3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da1d3-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="da1d3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da1d3-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da1d3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="da1d3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="da1d3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da1d3-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1d3-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1d3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="da1d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1d3-127">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="da1d3-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="da1d3-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="da1d3-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="da1d3-129">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="da1d3-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




