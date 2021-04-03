---
title: Método Unadvise IReferenceClock
description: O método Unadvise cancela uma solicitação de notificação.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Método Unadvise Windows Media Format
- Método Unadvise Windows Media Format, interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, método Unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084226"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="79d4d-106">Método IReferenceClock:: Unadvise</span><span class="sxs-lookup"><span data-stu-id="79d4d-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="79d4d-107">O método **Unadvise** cancela uma solicitação de notificação.</span><span class="sxs-lookup"><span data-stu-id="79d4d-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d4d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79d4d-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="79d4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79d4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d4d-110">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="79d4d-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="79d4d-111">Identificador da solicitação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="79d4d-111">Identifier of the request to remove.</span></span> <span data-ttu-id="79d4d-112">Use o valor retornado por AdviseTime no parâmetro pdwAdviseCookie.</span><span class="sxs-lookup"><span data-stu-id="79d4d-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79d4d-113">Return value</span></span>

<span data-ttu-id="79d4d-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="79d4d-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="79d4d-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="79d4d-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="79d4d-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="79d4d-116">Return code</span></span>                                                                             | <span data-ttu-id="79d4d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="79d4d-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="79d4d-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79d4d-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="79d4d-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="79d4d-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="79d4d-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="79d4d-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="79d4d-121">O identificador passado não existe.</span><span class="sxs-lookup"><span data-stu-id="79d4d-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="79d4d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="79d4d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d4d-123">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="79d4d-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





