---
description: Encerra as operações de gravação da lista especificada.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Função SdbEndWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762861"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="29702-103">Função SdbEndWriteListTag</span><span class="sxs-lookup"><span data-stu-id="29702-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="29702-104">Encerra as operações de gravação da lista especificada.</span><span class="sxs-lookup"><span data-stu-id="29702-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="29702-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29702-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="29702-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29702-107">*PDB* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="29702-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29702-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="29702-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="29702-109">*tiList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29702-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29702-110">O [**TagId**](tagid.md) da lista</span><span class="sxs-lookup"><span data-stu-id="29702-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29702-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29702-111">Return value</span></span>

<span data-ttu-id="29702-112">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="29702-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="29702-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="29702-113">Remarks</span></span>

<span data-ttu-id="29702-114">Chame essa função depois de gravar todas as entradas da lista; Ele marcará o final da lista.</span><span class="sxs-lookup"><span data-stu-id="29702-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="29702-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29702-115">Requirements</span></span>



| <span data-ttu-id="29702-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="29702-116">Requirement</span></span> | <span data-ttu-id="29702-117">Valor</span><span class="sxs-lookup"><span data-stu-id="29702-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29702-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29702-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29702-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29702-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29702-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29702-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29702-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29702-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29702-122">DLL</span><span class="sxs-lookup"><span data-stu-id="29702-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29702-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29702-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29702-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="29702-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29702-125">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="29702-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="29702-126">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="29702-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="29702-127">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="29702-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




