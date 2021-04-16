---
description: A função GetNPPEtypeSapFilter recupera o filtro ETYPE/SAP de um determinado BLOB.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Função GetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758592"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="954c4-103">Função GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="954c4-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="954c4-104">A função **GetNPPEtypeSapFilter** recupera o filtro ETYPE/SAP de um determinado BLOB.</span><span class="sxs-lookup"><span data-stu-id="954c4-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="954c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="954c4-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="954c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="954c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="954c4-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="954c4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-108">Identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="954c4-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-109">*pnSaps* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-110">Ponteiro para o número retornado de protocolos na tabela SAP.</span><span class="sxs-lookup"><span data-stu-id="954c4-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-111">*pnEtypes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-112">Ponteiro para o número retornado de ETYPEs na tabela ETYPE.</span><span class="sxs-lookup"><span data-stu-id="954c4-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-113">*ppSapTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-114">Ponteiro para a tabela SAP retornada.</span><span class="sxs-lookup"><span data-stu-id="954c4-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-115">*ppEtypeTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-116">Ponteiro para a tabela de ETYPE retornada.</span><span class="sxs-lookup"><span data-stu-id="954c4-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-117">*pFilterFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-118">Ponteiro para os sinalizadores de filtro retornados.</span><span class="sxs-lookup"><span data-stu-id="954c4-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="954c4-119">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="954c4-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="954c4-120">Identificador para um BLOB de erro, que especifica o local no BLOB original onde o erro (se houver) ocorreu.</span><span class="sxs-lookup"><span data-stu-id="954c4-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="954c4-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="954c4-121">Return value</span></span>

<span data-ttu-id="954c4-122">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="954c4-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="954c4-123">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="954c4-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="954c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="954c4-124">Remarks</span></span>

<span data-ttu-id="954c4-125">As informações de ETYPE/SAP são armazenadas na categoria de **configuração** da seção de **proprietário** NPP.</span><span class="sxs-lookup"><span data-stu-id="954c4-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="954c4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="954c4-126">Requirements</span></span>



| <span data-ttu-id="954c4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="954c4-127">Requirement</span></span> | <span data-ttu-id="954c4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="954c4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="954c4-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="954c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="954c4-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="954c4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="954c4-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="954c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="954c4-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="954c4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="954c4-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="954c4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="954c4-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="954c4-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="954c4-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="954c4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="954c4-136"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="954c4-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="954c4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="954c4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="954c4-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="954c4-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="954c4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="954c4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954c4-140">SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="954c4-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




