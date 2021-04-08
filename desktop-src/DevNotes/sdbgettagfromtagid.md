---
description: Recupera a marca associada ao TAGID especificado.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Função SdbGetTagFromTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089179"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="8e1fd-103">Função SdbGetTagFromTagID</span><span class="sxs-lookup"><span data-stu-id="8e1fd-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="8e1fd-104">Recupera a marca associada ao **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="8e1fd-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e1fd-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="8e1fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e1fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1fd-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e1fd-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1fd-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="8e1fd-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8e1fd-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e1fd-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1fd-110">O **TagId** para a marca.</span><span class="sxs-lookup"><span data-stu-id="8e1fd-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1fd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e1fd-111">Return value</span></span>

<span data-ttu-id="8e1fd-112">A função retorna a marca.</span><span class="sxs-lookup"><span data-stu-id="8e1fd-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1fd-113">Requirements</span></span>



| <span data-ttu-id="8e1fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1fd-114">Requirement</span></span> | <span data-ttu-id="8e1fd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8e1fd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1fd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e1fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1fd-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8e1fd-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8e1fd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e1fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1fd-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e1fd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8e1fd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1fd-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1fd-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1fd-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1fd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e1fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1fd-123">**Tags**</span><span class="sxs-lookup"><span data-stu-id="8e1fd-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="8e1fd-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="8e1fd-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




