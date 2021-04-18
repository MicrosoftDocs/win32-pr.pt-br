---
description: As \_ constantes LINEOPENOPTION listam as opções disponíveis para abrir uma linha.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes de LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779453"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="041c0-103">\_Constantes LINEOPENOPTION</span><span class="sxs-lookup"><span data-stu-id="041c0-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="041c0-104">As **\_ constantes LINEOPENOPTION** listam as opções disponíveis para abrir uma linha.</span><span class="sxs-lookup"><span data-stu-id="041c0-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="041c0-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**</span><span class="sxs-lookup"><span data-stu-id="041c0-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041c0-106">O aplicativo está disposto a lidar com solicitações de outros aplicativos que têm a linha aberta.</span><span class="sxs-lookup"><span data-stu-id="041c0-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="041c0-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**</span><span class="sxs-lookup"><span data-stu-id="041c0-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="041c0-108">O aplicativo deve ser informado sobre novas chamadas criadas no dispositivo de linha somente se essas chamadas aparecerem no endereço especificado no membro **dwAddressID** na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) apontada pelo parâmetro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="041c0-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="041c0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="041c0-109">Remarks</span></span>

<span data-ttu-id="041c0-110">Consulte [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obter mais detalhes sobre a operação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="041c0-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="041c0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="041c0-111">Requirements</span></span>



| <span data-ttu-id="041c0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="041c0-112">Requirement</span></span> | <span data-ttu-id="041c0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="041c0-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="041c0-114">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="041c0-114">TAPI version</span></span><br/> | <span data-ttu-id="041c0-115">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="041c0-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="041c0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="041c0-116">Header</span></span><br/>       | <dl> <span data-ttu-id="041c0-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="041c0-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




