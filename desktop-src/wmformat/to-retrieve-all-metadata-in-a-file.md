---
title: Para recuperar todos os metadados em um arquivo
description: Para recuperar todos os metadados em um arquivo
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows SDK de formato de mídia, Recuperando metadados
- ASF (Advanced Systems Format), Recuperando metadados
- ASF (formato de sistemas avançados), Recuperando metadados
- metadados, recuperando todos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fab81f151cbb661cc7769128e2d4371dd0b24869317d1888769ed66a60de86f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807466"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>Para recuperar todos os metadados em um arquivo

O exemplo de código a seguir é uma função que exibe todos os metadados em um arquivo. Para usar a função, você deve passar um ponteiro para a interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) de um objeto editor de metadados, objeto leitor, objeto leitor síncrono ou objeto gravador. Você também deve incluir o arquivo de cabeçalho stdio. h em algum lugar em seu projeto. Para obter mais informações sobre como usar este exemplo, consulte [usando os exemplos de código](using-the-code-examples.md).

Para maior clareza, este exemplo não exibe os valores dos atributos Binary e GUID. Para atributos binários, você deve verificar se o nome do atributo corresponde a qualquer um dos atributos de metadados complexos conhecidos. Se tiver, você deverá Formatar a saída de acordo com a estrutura usada para esse atributo. Da mesma forma, os valores de atributo GUID podem ser exibidos de várias maneiras. Você pode optar por exibir cada membro da estrutura um de cada vez ou converter a estrutura em uma cadeia de caracteres e exibi-la como um valor.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recuperando atributos de metadados**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




