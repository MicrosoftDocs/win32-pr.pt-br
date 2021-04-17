---
description: As \_ constantes LINELOCATIONOPTION definem os valores usados no membro dwOptions da estrutura LINELOCATIONENTRY retornada como parte da estrutura LINETRANSLATECAPS retornada por lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes de LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753536"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="54952-103">\_Constantes LINELOCATIONOPTION</span><span class="sxs-lookup"><span data-stu-id="54952-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="54952-104">As **constantes \_ LINELOCATIONOPTION** definem os valores usados no membro **dwOptions** da estrutura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) retornada como parte da estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retornada por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="54952-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="54952-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**</span><span class="sxs-lookup"><span data-stu-id="54952-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="54952-106">O modo de discagem padrão neste local é a discagem de pulso.</span><span class="sxs-lookup"><span data-stu-id="54952-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="54952-107">Se esse bit for definido, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirá um modificador de discagem "P" no início da cadeia de caracteres de seqüência retornada quando esse local for selecionado.</span><span class="sxs-lookup"><span data-stu-id="54952-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="54952-108">Se esse bit não estiver definido, **lineTranslateAddress** inserirá um modificador de discagem "T" no início da cadeia de caracteres de seqüência.</span><span class="sxs-lookup"><span data-stu-id="54952-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54952-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="54952-109">Remarks</span></span>

<span data-ttu-id="54952-110">Não extensível.</span><span class="sxs-lookup"><span data-stu-id="54952-110">Not extensible.</span></span> <span data-ttu-id="54952-111">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="54952-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="54952-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54952-112">Requirements</span></span>



| <span data-ttu-id="54952-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="54952-113">Requirement</span></span> | <span data-ttu-id="54952-114">Valor</span><span class="sxs-lookup"><span data-stu-id="54952-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="54952-115">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="54952-115">TAPI version</span></span><br/> | <span data-ttu-id="54952-116">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="54952-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="54952-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54952-117">Header</span></span><br/>       | <dl> <span data-ttu-id="54952-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="54952-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




