---
title: Usando atributos de metadados complexos
description: Usando atributos de metadados complexos
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- SDK do Windows Media Format, atributos de metadados complexos
- ASF (Advanced Systems Format), atributos de metadados complexos
- ASF (formato de sistemas avançados), atributos de metadados complexos
- metadados, atributos complexos
- atributos de metadados complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293774"
---
# <a name="using-complex-metadata-attributes"></a><span data-ttu-id="5ba67-108">Usando atributos de metadados complexos</span><span class="sxs-lookup"><span data-stu-id="5ba67-108">Using Complex Metadata Attributes</span></span>

<span data-ttu-id="5ba67-109">O SDK do Windows Media Format dá suporte a atributos de metadados complexos, que são atributos que têm valores representados por uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="5ba67-109">The Windows Media Format SDK supports complex metadata attributes, which are attributes that have values represented by a structure.</span></span> <span data-ttu-id="5ba67-110">Como todos os atributos devem ter um tipo de dados definido na enumeração [**WMT \_ attr \_ DataType**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) , todos os atributos de metadados complexos são tratados como **\_ \_ binários de tipo WMT**.</span><span class="sxs-lookup"><span data-stu-id="5ba67-110">Because all attributes must have a data type defined in the [**WMT\_ATTR\_DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) enumeration, all complex metadata attributes are treated as **WMT\_TYPE\_BINARY**.</span></span> <span data-ttu-id="5ba67-111">Ao escrever um atributo complexo, converta o ponteiro para a estrutura como um ponteiro de byte.</span><span class="sxs-lookup"><span data-stu-id="5ba67-111">When writing a complex attribute, cast the pointer to the structure as a byte pointer.</span></span> <span data-ttu-id="5ba67-112">Quando você recupera um atributo complexo, converta a matriz de bytes definida por [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) como a estrutura apropriada.</span><span class="sxs-lookup"><span data-stu-id="5ba67-112">When you retrieve a complex attribute, cast the array of bytes set by [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) as the appropriate structure.</span></span>

<span data-ttu-id="5ba67-113">Os exemplos de código a seguir mostram como definir e recuperar um atributo de metadados complexo.</span><span class="sxs-lookup"><span data-stu-id="5ba67-113">The following code examples show how to set and retrieve a complex metadata attribute.</span></span> <span data-ttu-id="5ba67-114">A primeira função adiciona um atributo de texto de usuário, a segunda função recupera um.</span><span class="sxs-lookup"><span data-stu-id="5ba67-114">The first function adds a user text attribute, the second function retrieves one.</span></span> <span data-ttu-id="5ba67-115">Para obter mais informações sobre como usar esses exemplos, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="5ba67-115">For more information about how to use these examples, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="5ba67-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ba67-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ba67-117">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="5ba67-117">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




