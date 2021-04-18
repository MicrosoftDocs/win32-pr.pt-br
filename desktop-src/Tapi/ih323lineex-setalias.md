---
description: O método setalias configura um alias H. 323 padrão para o endereço. Esse alias será usado no intercâmbio de configuração de chamada H. 323 para que a outra parte saiba o nome dessa entidade.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'Método IH323LineEx:: setalias (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800033"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="7d5d2-104">Método IH323LineEx:: setalias</span><span class="sxs-lookup"><span data-stu-id="7d5d2-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="7d5d2-105">\[**Setalias** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7d5d2-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7d5d2-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7d5d2-107">O método **setalias** configura um alias H. 323 padrão para o endereço.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="7d5d2-108">Esse alias será usado no intercâmbio de configuração de chamada H. 323 para que a outra parte saiba o nome dessa entidade.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="7d5d2-109">Chamar esse método uma segunda vez substituirá o alias anterior.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="7d5d2-110">O alias definido nessa interface será usado somente quando não houver outra maneira para o TSP encontrar um alias adequado.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="7d5d2-111">No futuro, quando o suporte do gatekeeper for adicionado ao TSP, o alias registrado no gatekeeper ou atribuído pelo gatekeeper substituirá o que for definido por meio desse método.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5d2-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d5d2-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="7d5d2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d5d2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d5d2-114">*strAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d5d2-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d5d2-115">O alias a ser usado, em Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="7d5d2-116">Terminação **nula** não é necessária.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="7d5d2-117">*dwLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d5d2-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d5d2-118">O comprimento do nome do alias em número de caracteres, incluindo o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="7d5d2-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d5d2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d5d2-119">Return value</span></span>

<span data-ttu-id="7d5d2-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-120">This method can return one of these values.</span></span>



| <span data-ttu-id="7d5d2-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7d5d2-121">Return code</span></span>                                                                               | <span data-ttu-id="7d5d2-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d2-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d5d2-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d2-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7d5d2-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7d5d2-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="7d5d2-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d2-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7d5d2-126">O número de caracteres indicado em *dwLength* excede o número real de caracteres no parâmetro *strAlias* .</span><span class="sxs-lookup"><span data-stu-id="7d5d2-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7d5d2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d5d2-127">Requirements</span></span>



| <span data-ttu-id="7d5d2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d5d2-128">Requirement</span></span> | <span data-ttu-id="7d5d2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7d5d2-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d2-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="7d5d2-130">TAPI version</span></span><br/> | <span data-ttu-id="7d5d2-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7d5d2-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7d5d2-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d5d2-132">Header</span></span><br/>       | <dl> <span data-ttu-id="7d5d2-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d2-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="7d5d2-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d5d2-134">Library</span></span><br/>      | <dl> <span data-ttu-id="7d5d2-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d2-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7d5d2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7d5d2-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="7d5d2-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d2-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




