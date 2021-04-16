---
description: O tipo de endereço identifica o formato de endereço, como número de telefone padrão ou endereço de email. Somente os aplicativos que negociam a TAPI versão 3,0 ou superior podem usar tipos de endereço.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Constantes de LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758403"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="825d7-104">\_Constantes LINEADDRESSTYPE</span><span class="sxs-lookup"><span data-stu-id="825d7-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="825d7-105">O tipo de endereço identifica o formato de endereço, como número de telefone padrão ou endereço de email.</span><span class="sxs-lookup"><span data-stu-id="825d7-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="825d7-106">Somente os aplicativos que negociam a TAPI versão 3,0 ou superior podem usar tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="825d7-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="825d7-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="825d7-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="825d7-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="825d7-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="825d7-109">O tipo de endereço é um número de telefone padrão.</span><span class="sxs-lookup"><span data-stu-id="825d7-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="825d7-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**SDP de LINEADDRESSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="825d7-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="825d7-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="825d7-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="825d7-112">O tipo de endereço é a conferência SDP (Session description Protocol).</span><span class="sxs-lookup"><span data-stu-id="825d7-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="825d7-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EmailName**</span><span class="sxs-lookup"><span data-stu-id="825d7-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="825d7-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="825d7-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="825d7-115">O tipo de endereço é um nome de email.</span><span class="sxs-lookup"><span data-stu-id="825d7-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="825d7-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ nome_do_domínio**</span><span class="sxs-lookup"><span data-stu-id="825d7-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="825d7-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="825d7-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="825d7-118">O tipo de endereço é um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="825d7-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="825d7-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**\_IPAddress LINEADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="825d7-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="825d7-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="825d7-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="825d7-121">O tipo de endereço é um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="825d7-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="825d7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="825d7-122">Requirements</span></span>



| <span data-ttu-id="825d7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="825d7-123">Requirement</span></span> | <span data-ttu-id="825d7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="825d7-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="825d7-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="825d7-125">TAPI version</span></span><br/> | <span data-ttu-id="825d7-126">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="825d7-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="825d7-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="825d7-127">Header</span></span><br/>       | <dl> <span data-ttu-id="825d7-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="825d7-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




