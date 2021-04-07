---
description: Verifica a existência de todos os assinantes transitórios no repositório de dados. Ao chamar esse método, você pode garantir que todos os assinantes transitórios listados no repositório de dados estejam ativos.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Método IEventSystem2:: VerifyTransientSubscribers'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920301"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="02344-104">Método IEventSystem2:: VerifyTransientSubscribers</span><span class="sxs-lookup"><span data-stu-id="02344-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="02344-105">Verifica a existência de todos os assinantes transitórios no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="02344-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="02344-106">Ao chamar esse método, você pode garantir que todos os assinantes transitórios listados no repositório de dados estejam ativos.</span><span class="sxs-lookup"><span data-stu-id="02344-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="02344-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02344-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="02344-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02344-108">Parameters</span></span>

<span data-ttu-id="02344-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="02344-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02344-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02344-110">Return value</span></span>

<span data-ttu-id="02344-111">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02344-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="02344-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02344-112">Requirements</span></span>



| <span data-ttu-id="02344-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="02344-113">Requirement</span></span> | <span data-ttu-id="02344-114">Valor</span><span class="sxs-lookup"><span data-stu-id="02344-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="02344-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02344-115">Minimum supported client</span></span><br/> | <span data-ttu-id="02344-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02344-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02344-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02344-117">Minimum supported server</span></span><br/> | <span data-ttu-id="02344-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02344-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="02344-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="02344-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02344-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="02344-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




