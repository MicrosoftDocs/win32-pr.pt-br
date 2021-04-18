---
description: A taxa ou a largura de banda de uma chamada especifica a velocidade da transmissão de dados. Três pontos de dados identificam a taxa atual a taxa máxima para um modo de portador especificado e a taxa mínima para o modo de portador.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarifa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764755"
---
# <a name="rate"></a><span data-ttu-id="ff871-104">Tarifa</span><span class="sxs-lookup"><span data-stu-id="ff871-104">Rate</span></span>

<span data-ttu-id="ff871-105">A taxa (ou largura de banda) de uma chamada especifica a velocidade da transmissão de dados.</span><span class="sxs-lookup"><span data-stu-id="ff871-105">The rate (or bandwidth) of a call specifies the speed of data transmission.</span></span> <span data-ttu-id="ff871-106">Três pontos de dados identificam a taxa: a taxa atual, a taxa máxima para um modo de portador especificado e a taxa mínima para o modo de portador.</span><span class="sxs-lookup"><span data-stu-id="ff871-106">Three data points identify rate: the current rate, the maximum rate for a specified bearer mode, and the minimum rate for the bearer mode.</span></span>

<span data-ttu-id="ff871-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="ff871-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="ff871-108">\* \* TAPI 2. x: \* \*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** ou **dwMaxRate** membro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="ff871-108">\*\*TAPI 2.x:  \*\*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** or **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="ff871-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ MAXRATE**, **cil \_ MINRATE** ou membro **de \_ taxa de cil** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="ff871-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_MAXRATE**, **CIL\_MINRATE**, or **CIL\_RATE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

<span data-ttu-id="ff871-110">\* \* TSPI: \* \*[**mensagem \_ CALLINFO de linha**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , com *dwParam1* definido como \_ taxa de LINECALLINFOSTATE</span><span class="sxs-lookup"><span data-stu-id="ff871-110">\*\*TSPI:  \*\*[**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_RATE</span></span>

 

 
