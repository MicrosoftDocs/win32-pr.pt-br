---
description: Define o filtro do BLOB ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Função SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296641"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="99df7-103">Função SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="99df7-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="99df7-104">A função **SetNPPEtypeSapFilter** define o filtro do blob ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="99df7-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="99df7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99df7-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="99df7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99df7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99df7-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-108">Um identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="99df7-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-109">*nSaps* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-110">O número de SAPs.</span><span class="sxs-lookup"><span data-stu-id="99df7-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-111">*nEtypes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-112">O número de ETYPEs na tabela ETYPE que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="99df7-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-113">*lpSapTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-114">Um ponteiro para a tabela SAP que está definida.</span><span class="sxs-lookup"><span data-stu-id="99df7-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-115">*lpEtypeTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-116">Um ponteiro para a tabela ETYPE definida.</span><span class="sxs-lookup"><span data-stu-id="99df7-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-117">*FilterFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99df7-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-118">Os sinalizadores de filtro definidos.</span><span class="sxs-lookup"><span data-stu-id="99df7-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="99df7-119">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99df7-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99df7-120">O identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="99df7-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99df7-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99df7-121">Return value</span></span>

<span data-ttu-id="99df7-122">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="99df7-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="99df7-123">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="99df7-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="99df7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99df7-124">Requirements</span></span>



| <span data-ttu-id="99df7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="99df7-125">Requirement</span></span> | <span data-ttu-id="99df7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="99df7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99df7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99df7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99df7-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99df7-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="99df7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99df7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99df7-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99df7-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99df7-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99df7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="99df7-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99df7-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="99df7-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99df7-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="99df7-134"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99df7-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="99df7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="99df7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99df7-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99df7-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99df7-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="99df7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99df7-138">GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="99df7-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




