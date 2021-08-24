---
description: Especifica uma lista de identificadores de idioma que especifica os idiomas contidos em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao Objeto de Lista de Idiomas, definido na especificação do ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: MF_PD_ASF_LANGLIST atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba22004001df2ba6be8fb7a173a3ea9bed1b0a73863ae111e61d36efa853e079
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119103698"
---
# <a name="mf_pd_asf_langlist-attribute"></a>Atributo \_ \_ LANGLIST do MF PD ASF \_

Especifica uma lista de identificadores de idioma que especifica os idiomas contidos em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao Objeto de Lista de Idiomas, definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo do header do Objeto de Lista de Idiomas. A tabela a seguir mostra o formato do blob:



| Campo Objeto de Lista de Idiomas | Tipo de dados    | Tamanho    | Descrição                            |
|----------------------------|--------------|---------|----------------------------------------|
| Contagem de registros de ID de idioma  | **DWORD**    | 4 bytes | Número de idiomas                    |
| Registros de ID de Idioma        | **Byte**\[\] | Varia  | Matriz de cadeias de caracteres de linguagem (veja abaixo). |



 

A primeira **DWORD** é o número de idiomas, seguido por uma matriz de cadeias de caracteres de identificador de idioma. Cada cadeia de caracteres tem o seguinte formato:



| Campo Objeto de Lista de Idiomas | Tipo de dados     | Tamanho    | Descrição                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Comprimento da ID da Linguagem         | **DWORD**     | 4 bytes | O comprimento da cadeia de caracteres em bytes, incluindo o tamanho do caractere **NULL à** frente. |
| ID do idioma                | **Wchar**\[\] | Varia  | Uma cadeia de caracteres terminada em nulo que contém o nome da linguagem RFC 1766.                           |



 

Cada cadeia de caracteres é uma marca de idioma em conformidade com o RFC 1766.

Para obter a marca de idioma de um fluxo específico no arquivo ASF, consulte o descritor de fluxo para o atributo [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX.**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> <dt>

Objeto de header ASF
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




