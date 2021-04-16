---
description: A \_ constante de sinalizador de bit LINETRANSLATEOPTION descreve uma opção usada pela conversão de endereços.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Constantes de LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779897"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="4425a-103">\_Constantes LINETRANSLATEOPTION</span><span class="sxs-lookup"><span data-stu-id="4425a-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="4425a-104">A constante de sinalizador de bit **LINETRANSLATEOPTION \_** descreve uma opção usada pela conversão de endereços.</span><span class="sxs-lookup"><span data-stu-id="4425a-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="4425a-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**</span><span class="sxs-lookup"><span data-stu-id="4425a-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4425a-106">Se uma cadeia de caracteres de espera de chamada de cancelamento for definida para o local, definir esse bit fará com que essa cadeia de caracteres seja inserida no início da cadeia de caracteres de discagem.</span><span class="sxs-lookup"><span data-stu-id="4425a-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="4425a-107">Isso é comumente usado por aplicativos de fax e de modem de dados para evitar a interrupção de chamadas por alarmes de espera de chamada.</span><span class="sxs-lookup"><span data-stu-id="4425a-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="4425a-108">Se nenhuma cadeia de caracteres de espera de chamada de cancelamento for definida para o local, esse bit não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="4425a-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="4425a-109">Observe que os aplicativos que usam esse bit também são aconselhados a definir o \_ bit seguro LINECALLPARAMFLAGS no membro **dwCallParamFlags** da estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passada para [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) por meio do parâmetro *lpCallParams* , de forma que, se o dispositivo de linha usar um mecanismo diferente de dígitos de discagem para suprimir as interrupções de chamada, esse mecanismo será invocado.</span><span class="sxs-lookup"><span data-stu-id="4425a-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4425a-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="4425a-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4425a-111">O cartão de chamada padrão deve ser substituído por um especificado.</span><span class="sxs-lookup"><span data-stu-id="4425a-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4425a-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**</span><span class="sxs-lookup"><span data-stu-id="4425a-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4425a-113">Essa opção força o endereço (número) a ser convertido como longa distância.</span><span class="sxs-lookup"><span data-stu-id="4425a-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4425a-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**</span><span class="sxs-lookup"><span data-stu-id="4425a-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4425a-115">Essa opção força o número (endereço) a ser traduzido como local.</span><span class="sxs-lookup"><span data-stu-id="4425a-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4425a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4425a-116">Remarks</span></span>

<span data-ttu-id="4425a-117">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="4425a-117">No extensibility.</span></span> <span data-ttu-id="4425a-118">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="4425a-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="4425a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4425a-119">Requirements</span></span>



| <span data-ttu-id="4425a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4425a-120">Requirement</span></span> | <span data-ttu-id="4425a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4425a-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4425a-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4425a-122">TAPI version</span></span><br/> | <span data-ttu-id="4425a-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4425a-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4425a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4425a-124">Header</span></span><br/>       | <dl> <span data-ttu-id="4425a-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4425a-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4425a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4425a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4425a-127">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="4425a-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="4425a-128">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="4425a-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="4425a-129">**LINETRANSLATEOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="4425a-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




