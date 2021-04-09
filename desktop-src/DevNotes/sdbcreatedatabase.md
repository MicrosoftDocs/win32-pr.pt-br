---
description: Cria um novo banco de dados de Shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Função SdbCreateDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920345"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="5795d-103">Função SdbCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="5795d-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="5795d-104">Cria um novo banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="5795d-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5795d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5795d-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="5795d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5795d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5795d-107">*pwszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5795d-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5795d-108">O caminho em que o banco de dados deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="5795d-108">The path where the database should be saved.</span></span> <span data-ttu-id="5795d-109">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5795d-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5795d-110">*ETYPE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5795d-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5795d-111">O tipo de caminho.</span><span class="sxs-lookup"><span data-stu-id="5795d-111">The path type.</span></span> <span data-ttu-id="5795d-112">Consulte [**\_ tipo de caminho**](path-type.md) para obter uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="5795d-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5795d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5795d-113">Return value</span></span>

<span data-ttu-id="5795d-114">A função retorna um identificador para o banco de dados Shim ou **nulo** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="5795d-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5795d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5795d-115">Requirements</span></span>



| <span data-ttu-id="5795d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5795d-116">Requirement</span></span> | <span data-ttu-id="5795d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5795d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5795d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5795d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5795d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5795d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5795d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5795d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5795d-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5795d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5795d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5795d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5795d-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5795d-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5795d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5795d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5795d-125">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="5795d-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




