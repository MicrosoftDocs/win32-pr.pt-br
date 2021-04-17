---
description: Especifica a matriz de canal, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5,1 para estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Propriedade MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763543"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="3e141-103">\_Propriedade MFPKEY WMRESAMP \_ CHANNELMTX</span><span class="sxs-lookup"><span data-stu-id="3e141-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="3e141-104">Especifica a matriz de canal, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5,1 para estéreo).</span><span class="sxs-lookup"><span data-stu-id="3e141-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3e141-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3e141-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3e141-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="3e141-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3e141-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3e141-107">Data Type</span></span>

<span data-ttu-id="3e141-108">\_Matriz VT i4 \| VT \_</span><span class="sxs-lookup"><span data-stu-id="3e141-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="3e141-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="3e141-109">Applies To</span></span>

-   [<span data-ttu-id="3e141-110">DSP de reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="3e141-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="3e141-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e141-111">Remarks</span></span>

<span data-ttu-id="3e141-112">O valor da propriedade é uma matriz de coeficientes do NS x nd, em que ns é o número de canais de origem e nd é o número de canais de destino.</span><span class="sxs-lookup"><span data-stu-id="3e141-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="3e141-113">Os coeficientes são especificados em decibéis usando a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="3e141-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="3e141-114">inteiro (65536 \* 20 \* log10 (DB))</span><span class="sxs-lookup"><span data-stu-id="3e141-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="3e141-115">A matriz é armazenada como uma matriz na ordem de linha principal, em que o número da linha é o canal de origem e o número da coluna é o canal de destino.</span><span class="sxs-lookup"><span data-stu-id="3e141-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="3e141-116">Portanto, se a matriz for a seguinte:</span><span class="sxs-lookup"><span data-stu-id="3e141-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="3e141-117">em seguida, você especificaria a matriz como:</span><span class="sxs-lookup"><span data-stu-id="3e141-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="3e141-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e141-118">Requirements</span></span>



| <span data-ttu-id="3e141-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e141-119">Requirement</span></span> | <span data-ttu-id="3e141-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3e141-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e141-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e141-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e141-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e141-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3e141-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e141-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e141-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e141-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e141-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e141-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e141-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e141-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e141-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e141-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e141-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e141-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
