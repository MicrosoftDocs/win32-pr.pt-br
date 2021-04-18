---
description: Recupera o índice para a marca especificada e o tipo de chave do banco de dados especificado.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Função SdbGetIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457002"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="7cbef-103">Função SdbGetIndex</span><span class="sxs-lookup"><span data-stu-id="7cbef-103">SdbGetIndex function</span></span>

<span data-ttu-id="7cbef-104">Recupera o índice para a marca especificada e o tipo de chave do banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="7cbef-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cbef-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7cbef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cbef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbef-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbef-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="7cbef-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="7cbef-109">*tWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbef-110">A marca.</span><span class="sxs-lookup"><span data-stu-id="7cbef-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="7cbef-111">*tKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbef-112">O tipo principal.</span><span class="sxs-lookup"><span data-stu-id="7cbef-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="7cbef-113">*lpdwFlags* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbef-114">Esse parâmetro pode ser 0 ou **SHIMDB \_ \_ \_ chave exclusiva do índice** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="7cbef-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbef-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cbef-115">Return value</span></span>

<span data-ttu-id="7cbef-116">O **TagId** do índice ou **TagId \_ nulo**.</span><span class="sxs-lookup"><span data-stu-id="7cbef-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cbef-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cbef-117">Remarks</span></span>

<span data-ttu-id="7cbef-118">O índice resultante pode ser usado para operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="7cbef-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cbef-119">Requirements</span></span>



| <span data-ttu-id="7cbef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbef-120">Requirement</span></span> | <span data-ttu-id="7cbef-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7cbef-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbef-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7cbef-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7cbef-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7cbef-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cbef-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7cbef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7cbef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cbef-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cbef-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




