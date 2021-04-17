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
# <a name="mf_pd_asf_langlist-attribute"></a>\_ \_ \_ Atributo langlist ASF PD MF

Especifica uma lista de identificadores de idioma que especifica os idiomas contidos em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto da lista de idiomas, definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo no cabeçalho de objeto da lista de idiomas. A tabela a seguir mostra o formato do blob:



| Campo de objeto de lista de idiomas | Tipo de dados    | Tamanho    | Descrição                            |
|----------------------------|--------------|---------|----------------------------------------|
| Contagem de registros de ID de idioma  | **DWORD**    | 4 bytes | Número de idiomas                    |
| Registros de ID de idioma        | **MINUCIOSA**\[\] | Varia  | Matriz de cadeias de caracteres de linguagem (veja abaixo). |



 

O primeiro **DWORD** é o número de idiomas, seguido por uma matriz de cadeias de caracteres de identificador de linguagem. Cada cadeia de caracteres tem o seguinte formato:



| Campo de objeto de lista de idiomas | Tipo de dados     | Tamanho    | Descrição                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Comprimento da ID de idioma         | **DWORD**     | 4 bytes | O comprimento da cadeia de caracteres em bytes, incluindo o tamanho do caractere **nulo** à direita. |
| ID do idioma                | **WCHAR**\[\] | Varia  | Uma cadeia de caracteres terminada em nulo que contém o nome do idioma RFC 1766.                           |



 

Cada cadeia de caracteres é uma marca de idioma compatível com RFC 1766.

Para obter a marca de idioma para um fluxo específico no arquivo ASF, consulte o descritor de fluxo para o atributo de [**\_ índice de ID de idioma MF SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como analisar a lista de idiomas.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

Objeto de cabeçalho ASF
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




