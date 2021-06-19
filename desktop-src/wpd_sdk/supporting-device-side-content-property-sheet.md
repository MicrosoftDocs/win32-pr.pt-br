---
title: Suporte ao conteúdo do lado do dispositivo (folha)
description: Saiba como usar a API do shell do Windows ou a API WPD para obter dados de objetos de dispositivo, que não podem ser acessados por meio do sistema de arquivos no Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404189"
---
# <a name="supporting-device-side-content"></a>Suporte ao conteúdo do lado do dispositivo

Como o conteúdo do lado do dispositivo não é acessível por meio do sistema de arquivos no Windows Vista, você precisará usar a API do shell do Windows ou a API WPD para recuperar dados de objetos de dispositivo. Essa é a principal diferença entre um manipulador de folhas de propriedades normal e um manipulador de folhas de propriedades WPD. O código de exemplo a seguir demonstra a recuperação do conteúdo do lado do dispositivo usando a API do shell do Windows.

A primeira etapa é a inicialização da lista de identificadores de item ou PIDL. (Essa lista contém o identificador exclusivo para o objeto de dispositivo fornecido.)


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



A função de inicialização chama a \_ função ExaminePIDLArray, que recupera as propriedades do objeto identificado por um PIDL na matriz PIDL.


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



Além da inicialização e do processamento da lista de identificadores de item, seu aplicativo precisará implementar o método IShellPropSheetExt:: ReplacePage e inserir os manipuladores de substituição apropriados. O Shell do Windows chama esse método cada vez que está prestes a exibir uma folha de propriedades substituível, dando ao seu aplicativo uma chance de invocar um manipulador de substituição correspondente. A palavra baixa do primeiro parâmetro para o método ReplacePage é um identificador para a folha de propriedades fornecida que o Windows está prestes a exibir. Os valores passados na palavra inferior do primeiro parâmetro correspondem aos valores definidos no arquivo WpdShellExtension. h. Esses valores e suas descrições aparecem na tabela a seguir.



| Valor                                  | Descrição                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ dispositivo \_ geral     | Corresponde à guia Geral do dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ armazenamento \_ geral    | Corresponde à guia geral de um objeto de armazenamento encontrado no dispositivo.    |
| \_ \_ conteúdo \_ geral do WPDNSE PROPSHEET    | Corresponde à guia Geral do objeto de conteúdo encontrado no dispositivo.      |
| WPDNSE \_ PROPSHEET \_ referências de conteúdo \_ | Corresponde à guia References de um objeto de conteúdo encontrado no dispositivo. |
| recursos de conteúdo do WPDNSE \_ PROPSHEET \_ \_  | Corresponde à guia de recursos de um objeto de conteúdo encontrado no dispositivo.  |
| detalhes do conteúdo do WPDNSE \_ PROPSHEET \_ \_    | Corresponde a uma guia de detalhes de um objeto de conteúdo encontrado no dispositivo.      |



 

Na extensão da folha de propriedades de exemplo, o método ReplacePage invoca dois manipuladores de substituição: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences. Esses manipuladores substituem as guias dispositivo geral e referências de conteúdo nas folhas de propriedades extensível.


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



Como é possível que um usuário Selecione vários dispositivos, um aplicativo precisará salvar a matriz PIDL retornada por IShellExtInit:: Initialize e, em seguida, examinar a palavra alta do primeiro parâmetro para ReplacePage. Um valor igual a zero nesta palavra alta corresponde ao primeiro elemento na matriz PIDL, um valor de um corresponde ao segundo elemento e assim por diante. Na função ReplacePage do aplicativo de exemplo, esse valor de palavra alta é passado para ambos os manipuladores de substituição. Esses manipuladores, por sua vez, usam esse valor para identificar um dispositivo específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



