---
description: As \_ constantes LINETONEMODE descrevem seleções diferentes que são usadas ao gerar tons de linha.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes de LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759963"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="5a7ec-103">\_Constantes LINETONEMODE</span><span class="sxs-lookup"><span data-stu-id="5a7ec-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="5a7ec-104">As **\_ constantes LINETONEMODE** descrevem seleções diferentes que são usadas ao gerar tons de linha.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="5a7ec-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_aviso sonoro de LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="5a7ec-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a7ec-106">O Tom é um aviso sonoro, como aquele usado para anunciar o início de uma gravação.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="5a7ec-107">A definição exata é um provedor de serviços definido.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a7ec-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**cobrança do LINETONEMODE \_**</span><span class="sxs-lookup"><span data-stu-id="5a7ec-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a7ec-109">O Tom é um tom de informações de cobrança, como um tom de pedido de cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="5a7ec-110">A definição exata é um provedor de serviços definido.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a7ec-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="5a7ec-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a7ec-112">O Tom é um tom ocupado.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-112">The tone is a busy tone.</span></span> <span data-ttu-id="5a7ec-113">A definição exata é um provedor de serviços definido.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a7ec-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizado**</span><span class="sxs-lookup"><span data-stu-id="5a7ec-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a7ec-115">O Tom é um tom personalizado definido por suas frequências de componente, do tipo [**lineGenerateTone**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span><span class="sxs-lookup"><span data-stu-id="5a7ec-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a7ec-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE de \_ toque**</span><span class="sxs-lookup"><span data-stu-id="5a7ec-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a7ec-117">O Tom é Tom de toque.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-117">The tone is ringback tone.</span></span> <span data-ttu-id="5a7ec-118">A definição exata é um provedor de serviços definido.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a7ec-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a7ec-119">Remarks</span></span>

<span data-ttu-id="5a7ec-120">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="5a7ec-121">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="5a7ec-122">Essas constantes são usadas para definir tons a serem gerados na faixa em uma chamada para a parte remota.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="5a7ec-123">Observe que a detecção de Tom de tons não personalizados não usa essas constantes.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a7ec-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a7ec-124">Requirements</span></span>



| <span data-ttu-id="5a7ec-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a7ec-125">Requirement</span></span> | <span data-ttu-id="5a7ec-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5a7ec-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5a7ec-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5a7ec-127">TAPI version</span></span><br/> | <span data-ttu-id="5a7ec-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5a7ec-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5a7ec-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a7ec-129">Header</span></span><br/>       | <dl> <span data-ttu-id="5a7ec-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a7ec-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




