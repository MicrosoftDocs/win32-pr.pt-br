---
description: Abre o banco de dados de shims especificado.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Função SdbOpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646238"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="ac6a3-103">Função SdbOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="ac6a3-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="ac6a3-104">Abre o banco de dados de shims especificado.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac6a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac6a3-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="ac6a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac6a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac6a3-107">*pwszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac6a3-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac6a3-108">O caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-108">The database path.</span></span> <span data-ttu-id="ac6a3-109">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ac6a3-110">*ETYPE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac6a3-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac6a3-111">O tipo de caminho.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-111">The path type.</span></span> <span data-ttu-id="ac6a3-112">Consulte [**\_ tipo de caminho**](path-type.md) para obter uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac6a3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac6a3-113">Return value</span></span>

<span data-ttu-id="ac6a3-114">A função retorna um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac6a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac6a3-115">Requirements</span></span>



| <span data-ttu-id="ac6a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac6a3-116">Requirement</span></span> | <span data-ttu-id="ac6a3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ac6a3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6a3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac6a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac6a3-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ac6a3-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac6a3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac6a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac6a3-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac6a3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac6a3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ac6a3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac6a3-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac6a3-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac6a3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac6a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6a3-125">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="ac6a3-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




