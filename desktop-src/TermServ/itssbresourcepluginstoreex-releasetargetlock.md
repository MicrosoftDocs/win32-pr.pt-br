---
title: Método ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Libera um bloqueio em um destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReleaseTargetLock
- Método ReleaseTargetLock Serviços de Área de Trabalho Remota, interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx, método ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085762"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="3ad31-106">Método ITsSbResourcePluginStoreEx:: ReleaseTargetLock</span><span class="sxs-lookup"><span data-stu-id="3ad31-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="3ad31-107">Libera um bloqueio em um destino.</span><span class="sxs-lookup"><span data-stu-id="3ad31-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad31-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ad31-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="3ad31-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ad31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad31-110">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ad31-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad31-111">Um ponteiro para o contexto retornado pelo método [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .</span><span class="sxs-lookup"><span data-stu-id="3ad31-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad31-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ad31-112">Return value</span></span>

<span data-ttu-id="3ad31-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3ad31-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ad31-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ad31-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad31-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ad31-115">Remarks</span></span>

<span data-ttu-id="3ad31-116">Esse método só está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="3ad31-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="3ad31-117">Esse método está disponível na interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partir do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3ad31-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad31-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad31-118">Requirements</span></span>



| <span data-ttu-id="3ad31-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad31-119">Requirement</span></span> | <span data-ttu-id="3ad31-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad31-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad31-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ad31-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad31-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ad31-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3ad31-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ad31-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad31-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ad31-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="3ad31-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3ad31-125">End of server support</span></span><br/>    | <span data-ttu-id="3ad31-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ad31-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="3ad31-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ad31-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ad31-128"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ad31-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="3ad31-129">IID</span><span class="sxs-lookup"><span data-stu-id="3ad31-129">IID</span></span><br/>                      | <span data-ttu-id="3ad31-130">IID \_ ITsSbResourcePluginStoreEx é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="3ad31-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ad31-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ad31-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad31-132">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="3ad31-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





