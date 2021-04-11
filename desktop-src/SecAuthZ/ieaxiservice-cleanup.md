---
description: Libera recursos usados pela interface IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Método IeAxiService:: Cleanup'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170652"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="44955-103">Método IeAxiService:: Cleanup</span><span class="sxs-lookup"><span data-stu-id="44955-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="44955-104">O método de **limpeza** libera os recursos usados pela interface [**IeAxiService**](ieaxiservice.md) .</span><span class="sxs-lookup"><span data-stu-id="44955-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="44955-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44955-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="44955-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44955-106">Parameters</span></span>

<span data-ttu-id="44955-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44955-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44955-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44955-108">Return value</span></span>

<span data-ttu-id="44955-109">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44955-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="44955-110">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="44955-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="44955-111">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="44955-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="44955-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44955-112">Requirements</span></span>



| <span data-ttu-id="44955-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="44955-113">Requirement</span></span> | <span data-ttu-id="44955-114">Valor</span><span class="sxs-lookup"><span data-stu-id="44955-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44955-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44955-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44955-116">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="44955-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44955-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44955-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44955-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="44955-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="44955-119">IID</span><span class="sxs-lookup"><span data-stu-id="44955-119">IID</span></span><br/>                      | <span data-ttu-id="44955-120">IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="44955-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="44955-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="44955-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44955-122">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="44955-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

