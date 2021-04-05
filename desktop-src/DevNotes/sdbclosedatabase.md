---
description: Fecha o banco de dados de shims especificado.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Função SdbCloseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010181"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="32f8e-103">Função SdbCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="32f8e-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="32f8e-104">Fecha o banco de dados de shims especificado.</span><span class="sxs-lookup"><span data-stu-id="32f8e-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32f8e-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="32f8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32f8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f8e-107">*PDB* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="32f8e-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32f8e-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="32f8e-108">A handle to the shim database.</span></span> <span data-ttu-id="32f8e-109">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="32f8e-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f8e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32f8e-110">Return value</span></span>

<span data-ttu-id="32f8e-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="32f8e-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f8e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f8e-112">Requirements</span></span>



| <span data-ttu-id="32f8e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f8e-113">Requirement</span></span> | <span data-ttu-id="32f8e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="32f8e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32f8e-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32f8e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="32f8e-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32f8e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="32f8e-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32f8e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="32f8e-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32f8e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="32f8e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="32f8e-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f8e-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f8e-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f8e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="32f8e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f8e-122">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="32f8e-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




