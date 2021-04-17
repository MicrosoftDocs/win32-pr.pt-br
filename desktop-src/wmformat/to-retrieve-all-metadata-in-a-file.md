---
title: Para recuperar todos os metadados em um arquivo
description: Para recuperar todos os metadados em um arquivo
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- SDK do Windows Media Format, Recuperando metadados
- ASF (Advanced Systems Format), Recuperando metadados
- ASF (formato de sistemas avançados), Recuperando metadados
- metadados, recuperando todos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc5d63a27cd4455d8d39cebee894dfbfc8d5bf2c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105770044"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a><span data-ttu-id="1e02a-107">Para recuperar todos os metadados em um arquivo</span><span class="sxs-lookup"><span data-stu-id="1e02a-107">To Retrieve All Metadata in a File</span></span>

<span data-ttu-id="1e02a-108">O exemplo de código a seguir é uma função que exibe todos os metadados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e02a-108">The following code example is a function that displays all the metadata in a file.</span></span> <span data-ttu-id="1e02a-109">Para usar a função, você deve passar um ponteiro para a interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) de um objeto editor de metadados, objeto leitor, objeto leitor síncrono ou objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="1e02a-109">In order to use the function, you must pass it a pointer to the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface of a metadata editor object, reader object, synchronous reader object, or writer object.</span></span> <span data-ttu-id="1e02a-110">Você também deve incluir o arquivo de cabeçalho stdio. h em algum lugar em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="1e02a-110">You must also include the Stdio.h header file somewhere in your project.</span></span> <span data-ttu-id="1e02a-111">Para obter mais informações sobre como usar este exemplo, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1e02a-111">For more information about how to use this example, see [Using the Code Examples](using-the-code-examples.md).</span></span>

<span data-ttu-id="1e02a-112">Para maior clareza, este exemplo não exibe os valores dos atributos Binary e GUID.</span><span class="sxs-lookup"><span data-stu-id="1e02a-112">For clarity, this example does not display the values of binary and GUID attributes.</span></span> <span data-ttu-id="1e02a-113">Para atributos binários, você deve verificar se o nome do atributo corresponde a qualquer um dos atributos de metadados complexos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="1e02a-113">For binary attributes, you should check to see if the attribute name matches any of the known complex metadata attributes.</span></span> <span data-ttu-id="1e02a-114">Se tiver, você deverá Formatar a saída de acordo com a estrutura usada para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="1e02a-114">If it does, you should format your output according to the structure used for that attribute.</span></span> <span data-ttu-id="1e02a-115">Da mesma forma, os valores de atributo GUID podem ser exibidos de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="1e02a-115">Similarly, GUID attribute values can be displayed in a number of ways.</span></span> <span data-ttu-id="1e02a-116">Você pode optar por exibir cada membro da estrutura um de cada vez ou converter a estrutura em uma cadeia de caracteres e exibi-la como um valor.</span><span class="sxs-lookup"><span data-stu-id="1e02a-116">You can choose to display each member of the structure one at a time or convert the structure to a string and display it as one value.</span></span>


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="1e02a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e02a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e02a-118">**Recuperando atributos de metadados**</span><span class="sxs-lookup"><span data-stu-id="1e02a-118">**Retrieving Metadata Attributes**</span></span>](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




