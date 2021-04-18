---
description: Dados de formato adicionais para um fluxo binário em um arquivo ASF (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Atributo MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793889"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="0532b-103">\_Atributo de \_ \_ formato arbitrário do MF MT</span><span class="sxs-lookup"><span data-stu-id="0532b-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="0532b-104">Dados de formato adicionais para um fluxo binário em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="0532b-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="0532b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0532b-105">Data type</span></span>

<span data-ttu-id="0532b-106">**MINUCIOSA\[\]**</span><span class="sxs-lookup"><span data-stu-id="0532b-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="0532b-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0532b-107">Get/set</span></span>

<span data-ttu-id="0532b-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="0532b-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="0532b-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="0532b-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="0532b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0532b-110">Remarks</span></span>

<span data-ttu-id="0532b-111">Os aplicativos podem usar fluxos binários para manter tipos de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="0532b-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="0532b-112">A fonte de mídia do ASF trata o valor desse atributo como um blob opaco.</span><span class="sxs-lookup"><span data-stu-id="0532b-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="0532b-113">O membro **formatType** da estrutura [**de \_ \_ cabeçalho arbitrário MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) define o layout dos dados de formato.</span><span class="sxs-lookup"><span data-stu-id="0532b-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="0532b-114">Essa estrutura corresponde ao campo formatar dados dos dados específicos do tipo no objeto Propriedades do fluxo, em arquivos em que o tipo de fluxo é **\_ \_ mídia binária de ASF**.</span><span class="sxs-lookup"><span data-stu-id="0532b-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="0532b-115">Para obter mais informações, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="0532b-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="0532b-116">No SDK do Windows Media Format, os fluxos binários são chamados de *fluxos arbitrários* ou *fluxos de dados arbitrários*.</span><span class="sxs-lookup"><span data-stu-id="0532b-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="0532b-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0532b-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0532b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0532b-118">Requirements</span></span>



| <span data-ttu-id="0532b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0532b-119">Requirement</span></span> | <span data-ttu-id="0532b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0532b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0532b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0532b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0532b-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0532b-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0532b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0532b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0532b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0532b-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0532b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0532b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0532b-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0532b-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0532b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0532b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0532b-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0532b-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0532b-129">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="0532b-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="0532b-130">\_ \_ cabeçalho ARBITRÁRIO do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="0532b-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




