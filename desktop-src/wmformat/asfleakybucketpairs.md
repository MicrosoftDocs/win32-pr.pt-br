---
title: ASFLeakyBucketPairs
description: O atributo ASFLeakyBucketPairs é um atributo opcional que descreve os requisitos de buffer para um arquivo de taxa de bits variável.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Formato de mídia do Windows ASFLeakyBucketPairs
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105797576"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="1005e-104">ASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="1005e-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="1005e-105">O atributo **ASFLeakyBucketPairs** é um atributo opcional que descreve os requisitos de buffer para um arquivo de taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="1005e-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1005e-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="1005e-106">Global Constant</span></span>

<span data-ttu-id="1005e-107">g \_ wszASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="1005e-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="1005e-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1005e-108">Data Type</span></span>

<span data-ttu-id="1005e-109">**WMT \_ tipo \_ binário**</span><span class="sxs-lookup"><span data-stu-id="1005e-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="1005e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1005e-110">Remarks</span></span>

<span data-ttu-id="1005e-111">Esse atributo tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="1005e-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="1005e-112">Em que *wReserved* deve ser igual a zero e *Bucket* é uma matriz de estruturas de [**\_ \_ \_ pares de buckets de vazamento do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) .</span><span class="sxs-lookup"><span data-stu-id="1005e-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="1005e-113">A matriz deve conter pelo menos duas entradas, mas pode ser maior.</span><span class="sxs-lookup"><span data-stu-id="1005e-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="1005e-114">O objeto leitor usa esse atributo para determinar a quantidade de conteúdo a ser armazenada em buffer antes da reprodução.</span><span class="sxs-lookup"><span data-stu-id="1005e-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="1005e-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1005e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1005e-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="1005e-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




