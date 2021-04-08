---
description: Grava dados binários do arquivo especificado no banco de dado especificado.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Função SdbWriteBinaryTagFromFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920261"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="3560f-103">Função SdbWriteBinaryTagFromFile</span><span class="sxs-lookup"><span data-stu-id="3560f-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="3560f-104">Grava dados binários do arquivo especificado no banco de dado especificado.</span><span class="sxs-lookup"><span data-stu-id="3560f-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3560f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3560f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="3560f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3560f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3560f-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3560f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560f-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="3560f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3560f-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3560f-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560f-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="3560f-110">The TAG for the entry.</span></span> <span data-ttu-id="3560f-111">Essa marca deve ser do tipo **tipo de marca \_ \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="3560f-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="3560f-112">*pwszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3560f-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560f-113">O caminho para o arquivo que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="3560f-113">The path to the file that contains the data.</span></span> <span data-ttu-id="3560f-114">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3560f-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3560f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3560f-115">Return value</span></span>

<span data-ttu-id="3560f-116">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="3560f-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3560f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3560f-117">Requirements</span></span>



| <span data-ttu-id="3560f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3560f-118">Requirement</span></span> | <span data-ttu-id="3560f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3560f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3560f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3560f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3560f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3560f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3560f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3560f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3560f-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3560f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3560f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3560f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3560f-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3560f-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3560f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3560f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3560f-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3560f-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




