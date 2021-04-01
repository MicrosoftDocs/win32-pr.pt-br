---
description: Contém os nomes amigáveis dos estilos de intercâmbio de mídia acessível (SAMI) sincronizados definidos no arquivo SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Atributo MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837153"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="5d75e-103">Atributo de estilo ' MF \_ PD \_ samilist \_</span><span class="sxs-lookup"><span data-stu-id="5d75e-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="5d75e-104">Contém os nomes amigáveis dos estilos de intercâmbio de mídia acessível (SAMI) sincronizados definidos no arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="5d75e-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="5d75e-105">A [fonte de mídia Sami](sami-media-source.md) define esse atributo no descritor de apresentação que ele cria.</span><span class="sxs-lookup"><span data-stu-id="5d75e-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d75e-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5d75e-106">Data type</span></span>

<span data-ttu-id="5d75e-107">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="5d75e-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5d75e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d75e-108">Remarks</span></span>

<span data-ttu-id="5d75e-109">O blob de atributo tem a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="5d75e-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="5d75e-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5d75e-110">Data Type</span></span>

<span data-ttu-id="5d75e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d75e-111">Description</span></span>

<span data-ttu-id="5d75e-112">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="5d75e-112">Size (bytes)</span></span>

<span data-ttu-id="5d75e-113">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="5d75e-113">**DWORD**</span></span>

<span data-ttu-id="5d75e-114">Número de cadeias de caracteres de estilo.</span><span class="sxs-lookup"><span data-stu-id="5d75e-114">Number of style strings.</span></span>

<span data-ttu-id="5d75e-115">4</span><span class="sxs-lookup"><span data-stu-id="5d75e-115">4</span></span>

<span data-ttu-id="5d75e-116">Para cada cadeia de estilo:</span><span class="sxs-lookup"><span data-stu-id="5d75e-116">For each style string:</span></span>

<span data-ttu-id="5d75e-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="5d75e-117">**DWORD**</span></span>

<span data-ttu-id="5d75e-118">Tamanho da cadeia de caracteres em bytes, incluindo o caractere **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5d75e-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="5d75e-119">4</span><span class="sxs-lookup"><span data-stu-id="5d75e-119">4</span></span>

<span data-ttu-id="5d75e-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5d75e-120">**LPWSTR**</span></span>

<span data-ttu-id="5d75e-121">Cadeia de caracteres largo terminada em nulo que contém o nome do estilo.</span><span class="sxs-lookup"><span data-stu-id="5d75e-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="5d75e-122">Varia</span><span class="sxs-lookup"><span data-stu-id="5d75e-122">Varies</span></span>



 

<span data-ttu-id="5d75e-123">Para definir o estilo ou recuperar o estilo atual, use a interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="5d75e-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="5d75e-124">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5d75e-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="5d75e-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d75e-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5d75e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d75e-126">Requirements</span></span>



| <span data-ttu-id="5d75e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d75e-127">Requirement</span></span> | <span data-ttu-id="5d75e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5d75e-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d75e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d75e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d75e-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d75e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d75e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d75e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d75e-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d75e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d75e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d75e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d75e-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d75e-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d75e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d75e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d75e-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d75e-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d75e-137">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="5d75e-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5d75e-138">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="5d75e-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5d75e-139">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5d75e-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5d75e-140">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="5d75e-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d75e-141">Fonte de mídia SAMI</span><span class="sxs-lookup"><span data-stu-id="5d75e-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




