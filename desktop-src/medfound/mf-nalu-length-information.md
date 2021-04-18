---
description: Indica os comprimentos de NALUs no exemplo. Este é um BLOB MF que é definido em exemplos de entrada compactados para o decodificador H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Atributo MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807268"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="04bfd-104">\_Atributo de \_ informações de comprimento de MF NALU \_</span><span class="sxs-lookup"><span data-stu-id="04bfd-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="04bfd-105">Indica os comprimentos de NALUs no exemplo.</span><span class="sxs-lookup"><span data-stu-id="04bfd-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="04bfd-106">Este é um **blob** MF que é definido em exemplos de entrada compactados para o decodificador H. 264.</span><span class="sxs-lookup"><span data-stu-id="04bfd-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="04bfd-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="04bfd-107">Data type</span></span>

<span data-ttu-id="04bfd-108">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="04bfd-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="04bfd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="04bfd-109">Remarks</span></span>

<span data-ttu-id="04bfd-110">Para que esse atributo seja definido, a mídia deve ser do tipo MEDIASUBTYPE \_ H264 e o atributo de [ \_ conjunto de \_ comprimento \_ MF NALU](mf-nalu-length-set.md) deve ser definido no tipo de mídia de entrada de MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="04bfd-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="04bfd-111">Defina \_ informações de comprimento de NALU MF \_ \_ como um **blob** no exemplo de entrada, com um DWORD para cada NALU no exemplo.</span><span class="sxs-lookup"><span data-stu-id="04bfd-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="04bfd-112">Por exemplo, se houver AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), fatia de IDR 2 (60 k), deverá haver 5 DWORDs com os valores 9, 25, 10, 50 k, 60 k no **blob**.</span><span class="sxs-lookup"><span data-stu-id="04bfd-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="04bfd-113">Aqui, um código que define o **blob**, em que **rgdwNALULengthInfo** é uma matriz do tipo DWORD e **UINALULENGTHIDX** é o comprimento de NALU válido definido para o **blob**.</span><span class="sxs-lookup"><span data-stu-id="04bfd-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="04bfd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04bfd-114">Requirements</span></span>



| <span data-ttu-id="04bfd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bfd-115">Requirement</span></span> | <span data-ttu-id="04bfd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="04bfd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04bfd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bfd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="04bfd-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="04bfd-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="04bfd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bfd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="04bfd-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="04bfd-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="04bfd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04bfd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="04bfd-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04bfd-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04bfd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="04bfd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bfd-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04bfd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04bfd-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="04bfd-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




