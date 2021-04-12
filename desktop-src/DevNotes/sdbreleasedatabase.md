---
description: Fecha o banco de dados de Shim inicializado usando a função SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Função SdbReleaseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500871"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="ff7a9-103">Função SdbReleaseDatabase</span><span class="sxs-lookup"><span data-stu-id="ff7a9-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="ff7a9-104">Fecha o banco de dados de Shim inicializado usando a função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="ff7a9-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff7a9-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="ff7a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff7a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff7a9-107">*hSDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff7a9-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff7a9-108">Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="ff7a9-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff7a9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff7a9-109">Return value</span></span>

<span data-ttu-id="ff7a9-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff7a9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff7a9-111">Requirements</span></span>



| <span data-ttu-id="ff7a9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff7a9-112">Requirement</span></span> | <span data-ttu-id="ff7a9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ff7a9-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7a9-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff7a9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ff7a9-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff7a9-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff7a9-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff7a9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ff7a9-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff7a9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ff7a9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ff7a9-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff7a9-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff7a9-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7a9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff7a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7a9-121">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="ff7a9-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




