---
description: Especifica uma lista de identificadores de idioma que especifica os idiomas contidos em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto da lista de idiomas, definido na especificação do ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: Atributo MF_PD_ASF_LANGLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779984"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="d5be5-104">\_ \_ \_ Atributo langlist ASF PD MF</span><span class="sxs-lookup"><span data-stu-id="d5be5-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="d5be5-105">Especifica uma lista de identificadores de idioma que especifica os idiomas contidos em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d5be5-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="d5be5-106">Esse atributo corresponde ao objeto da lista de idiomas, definido na especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="d5be5-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5be5-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5be5-107">Data type</span></span>

<span data-ttu-id="d5be5-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="d5be5-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d5be5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5be5-109">Remarks</span></span>

<span data-ttu-id="d5be5-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="d5be5-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="d5be5-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo no cabeçalho de objeto da lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="d5be5-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="d5be5-112">A tabela a seguir mostra o formato do blob:</span><span class="sxs-lookup"><span data-stu-id="d5be5-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="d5be5-113">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="d5be5-113">Language List Object field</span></span> | <span data-ttu-id="d5be5-114">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5be5-114">Data type</span></span>    | <span data-ttu-id="d5be5-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d5be5-115">Size</span></span>    | <span data-ttu-id="d5be5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5be5-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="d5be5-117">Contagem de registros de ID de idioma</span><span class="sxs-lookup"><span data-stu-id="d5be5-117">Language ID Records Count</span></span>  | <span data-ttu-id="d5be5-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d5be5-118">**DWORD**</span></span>    | <span data-ttu-id="d5be5-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="d5be5-119">4 bytes</span></span> | <span data-ttu-id="d5be5-120">Número de idiomas</span><span class="sxs-lookup"><span data-stu-id="d5be5-120">Number of languages</span></span>                    |
| <span data-ttu-id="d5be5-121">Registros de ID de idioma</span><span class="sxs-lookup"><span data-stu-id="d5be5-121">Language ID Records</span></span>        | <span data-ttu-id="d5be5-122">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="d5be5-122">**BYTE**\[\]</span></span> | <span data-ttu-id="d5be5-123">Varia</span><span class="sxs-lookup"><span data-stu-id="d5be5-123">Varies</span></span>  | <span data-ttu-id="d5be5-124">Matriz de cadeias de caracteres de linguagem (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="d5be5-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="d5be5-125">O primeiro **DWORD** é o número de idiomas, seguido por uma matriz de cadeias de caracteres de identificador de linguagem.</span><span class="sxs-lookup"><span data-stu-id="d5be5-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="d5be5-126">Cada cadeia de caracteres tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="d5be5-126">Each string has the following format:</span></span>



| <span data-ttu-id="d5be5-127">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="d5be5-127">Language List Object field</span></span> | <span data-ttu-id="d5be5-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5be5-128">Data type</span></span>     | <span data-ttu-id="d5be5-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d5be5-129">Size</span></span>    | <span data-ttu-id="d5be5-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5be5-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5be5-131">Comprimento da ID de idioma</span><span class="sxs-lookup"><span data-stu-id="d5be5-131">Language ID Length</span></span>         | <span data-ttu-id="d5be5-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="d5be5-132">**DWORD**</span></span>     | <span data-ttu-id="d5be5-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="d5be5-133">4 bytes</span></span> | <span data-ttu-id="d5be5-134">O comprimento da cadeia de caracteres em bytes, incluindo o tamanho do caractere **nulo** à direita.</span><span class="sxs-lookup"><span data-stu-id="d5be5-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="d5be5-135">ID do idioma</span><span class="sxs-lookup"><span data-stu-id="d5be5-135">Language ID</span></span>                | <span data-ttu-id="d5be5-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="d5be5-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="d5be5-137">Varia</span><span class="sxs-lookup"><span data-stu-id="d5be5-137">Varies</span></span>  | <span data-ttu-id="d5be5-138">Uma cadeia de caracteres terminada em nulo que contém o nome do idioma RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="d5be5-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="d5be5-139">Cada cadeia de caracteres é uma marca de idioma compatível com RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="d5be5-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="d5be5-140">Para obter a marca de idioma para um fluxo específico no arquivo ASF, consulte o descritor de fluxo para o atributo de [**\_ índice de ID de idioma MF SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d5be5-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="d5be5-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5be5-141">Examples</span></span>

<span data-ttu-id="d5be5-142">O exemplo a seguir mostra como analisar a lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="d5be5-142">The following example shows how to parse the language list.</span></span>


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a><span data-ttu-id="d5be5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5be5-143">Requirements</span></span>



| <span data-ttu-id="d5be5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5be5-144">Requirement</span></span> | <span data-ttu-id="d5be5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d5be5-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5be5-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5be5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d5be5-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5be5-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5be5-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5be5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d5be5-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5be5-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5be5-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5be5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5be5-151"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5be5-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5be5-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5be5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5be5-153">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5be5-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5be5-154">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="d5be5-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d5be5-155">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="d5be5-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d5be5-156">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d5be5-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="d5be5-157">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="d5be5-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5be5-158">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="d5be5-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="d5be5-159">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="d5be5-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="d5be5-160">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="d5be5-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




