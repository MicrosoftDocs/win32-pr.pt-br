---
description: Retorna o número de elementos armazenados por este enumerador.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Método IEnumWiaItem2:: GetCount (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010599"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="d16fb-103">Método IEnumWiaItem2:: GetCount</span><span class="sxs-lookup"><span data-stu-id="d16fb-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="d16fb-104">Retorna o número de elementos armazenados por este enumerador.</span><span class="sxs-lookup"><span data-stu-id="d16fb-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d16fb-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="d16fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d16fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16fb-107">*cElt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d16fb-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d16fb-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="d16fb-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="d16fb-109">Recebe um ponteiro para um _ *ULONG*\* que recebe o número de elementos na enumeração.</span><span class="sxs-lookup"><span data-stu-id="d16fb-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16fb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d16fb-110">Return value</span></span>

<span data-ttu-id="d16fb-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d16fb-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d16fb-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d16fb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d16fb-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d16fb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d16fb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d16fb-114">Requirements</span></span>



| <span data-ttu-id="d16fb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d16fb-115">Requirement</span></span> | <span data-ttu-id="d16fb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d16fb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d16fb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d16fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d16fb-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d16fb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d16fb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d16fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d16fb-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d16fb-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d16fb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d16fb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16fb-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d16fb-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d16fb-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="d16fb-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d16fb-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d16fb-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




