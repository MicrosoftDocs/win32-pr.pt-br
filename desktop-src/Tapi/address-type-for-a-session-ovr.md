---
description: O tipo de endereço identifica o formato necessário para um endereço. Por exemplo, se o tipo for LINEADDRESSTYPE \_ PHONENUMBER, o endereço usado para discar na sessão deverá ser um número de telefone.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Tipo de endereço para uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783372"
---
# <a name="address-type-for-a-session"></a><span data-ttu-id="10a20-104">Tipo de endereço para uma sessão</span><span class="sxs-lookup"><span data-stu-id="10a20-104">Address Type for a Session</span></span>

<span data-ttu-id="10a20-105">O [**tipo de endereço**](lineaddresstype--constants.md) identifica o formato necessário para um endereço.</span><span class="sxs-lookup"><span data-stu-id="10a20-105">The [**address type**](lineaddresstype--constants.md) identifies the format required for an address.</span></span> <span data-ttu-id="10a20-106">Por exemplo, se o tipo for LINEADDRESSTYPE \_ PHONENUMBER, o endereço usado para discar na sessão deverá ser um número de telefone.</span><span class="sxs-lookup"><span data-stu-id="10a20-106">For example, if the type is LINEADDRESSTYPE\_PHONENUMBER, the address used to dial on the session must be a phone number.</span></span>

<span data-ttu-id="10a20-107">Um determinado dispositivo e provedor de serviços dá suporte A um ou mais tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="10a20-107">A given device and service provider supports one or more address types.</span></span> <span data-ttu-id="10a20-108">Consulte os [tipos de endereço para um dispositivo](address-type-ovr.md) para obter informações sobre como sondar um dispositivo para os formatos de endereço aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="10a20-108">See the [address types for a device](address-type-ovr.md) for information on how to poll a device for the address formats it supports.</span></span>

<span data-ttu-id="10a20-109">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), membro **dwAddressType** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="10a20-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="10a20-110">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o **membro \_ cil CALLERIDADDRESSTYPE**, **cil \_ CALLEDIDADDRESSTYPE** ou **cil \_ CONNECTEDIDADDRESSTYPE** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="10a20-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_CALLERIDADDRESSTYPE**, **CIL\_CALLEDIDADDRESSTYPE**, or **CIL\_CONNECTEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
