---
description: Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Método IContextTransactionInfo:: GetTxIsolationLevelAndTimeout'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783686"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="fa089-103">Método IContextTransactionInfo:: GetTxIsolationLevelAndTimeout</span><span class="sxs-lookup"><span data-stu-id="fa089-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="fa089-104">Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.</span><span class="sxs-lookup"><span data-stu-id="fa089-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa089-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa089-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="fa089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa089-107">*pIsoLevel* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa089-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa089-108">O valor [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) da transação.</span><span class="sxs-lookup"><span data-stu-id="fa089-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="fa089-109">*dwTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa089-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa089-110">O tempo limite da transação, em segundos.</span><span class="sxs-lookup"><span data-stu-id="fa089-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa089-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa089-111">Return value</span></span>

<span data-ttu-id="fa089-112">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa089-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa089-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa089-113">Requirements</span></span>



| <span data-ttu-id="fa089-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa089-114">Requirement</span></span> | <span data-ttu-id="fa089-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fa089-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fa089-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa089-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa089-117">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="fa089-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fa089-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa089-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa089-119">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="fa089-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa089-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa089-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa089-121">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="fa089-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

