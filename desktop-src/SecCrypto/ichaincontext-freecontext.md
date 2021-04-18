---
description: Libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Método IChainContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800081"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="2635b-103">Método IChainContext:: FreeContext</span><span class="sxs-lookup"><span data-stu-id="2635b-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="2635b-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="2635b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="2635b-105">O método **FreeContext** libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="2635b-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2635b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2635b-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="2635b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2635b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2635b-108">*pChainContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2635b-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2635b-109">O contexto da cadeia de PCCERT \_ \_ a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="2635b-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2635b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2635b-110">Return value</span></span>

<span data-ttu-id="2635b-111">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2635b-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="2635b-112">Um valor de S \_ OK indica êxito.</span><span class="sxs-lookup"><span data-stu-id="2635b-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="2635b-113">Qualquer outro valor indica que a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="2635b-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2635b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2635b-114">Remarks</span></span>

<span data-ttu-id="2635b-115">Esse método não libera o contexto de \_ cadeia de PCCERT \_ contido em um objeto de [**cadeia**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="2635b-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="2635b-116">Ele deve ser usado apenas para liberar um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="2635b-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2635b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2635b-117">Requirements</span></span>



| <span data-ttu-id="2635b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2635b-118">Requirement</span></span> | <span data-ttu-id="2635b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2635b-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2635b-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2635b-120">Redistributable</span></span><br/> | <span data-ttu-id="2635b-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2635b-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2635b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2635b-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="2635b-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2635b-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2635b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2635b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2635b-125">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="2635b-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




