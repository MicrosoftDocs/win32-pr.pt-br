---
description: Abre o banco de dados de detalhes de AppHelp especificado.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Função SdbOpenApphelpDetailsDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088812"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="6999f-103">Função SdbOpenApphelpDetailsDatabase</span><span class="sxs-lookup"><span data-stu-id="6999f-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="6999f-104">Abre o banco de dados de detalhes de AppHelp especificado.</span><span class="sxs-lookup"><span data-stu-id="6999f-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6999f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6999f-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="6999f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6999f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6999f-107">*pwsDetailsDatabasePath* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6999f-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6999f-108">O caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6999f-108">The database path.</span></span> <span data-ttu-id="6999f-109">Se esse parâmetro for **nulo**, o banco de dados do sistema local será aberto.</span><span class="sxs-lookup"><span data-stu-id="6999f-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6999f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6999f-110">Return value</span></span>

<span data-ttu-id="6999f-111">A função retorna um identificador para o banco de dados de detalhes de AppHelp.</span><span class="sxs-lookup"><span data-stu-id="6999f-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="6999f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6999f-112">Requirements</span></span>



| <span data-ttu-id="6999f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6999f-113">Requirement</span></span> | <span data-ttu-id="6999f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6999f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6999f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6999f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6999f-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6999f-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6999f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6999f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6999f-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6999f-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6999f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6999f-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6999f-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6999f-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




