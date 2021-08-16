---
title: Suporte ao conteúdo do lado do dispositivo (PropertySheet)
description: Saiba como usar a API Windows Shell do Windows ou a API WPD para obter dados para objetos de dispositivo, que não podem ser acessados por meio do sistema de arquivos no Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451bf63c1270b121cf909fa5ee07aff62cc3b83aa0e0d031cae61005f725c197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842563"
---
# <a name="supporting-device-side-content"></a>Suporte ao conteúdo do lado do dispositivo

Como o conteúdo do lado do dispositivo não está acessível por meio do sistema de arquivos no Windows Vista, você precisará usar a API do Shell do Windows ou a API wpd para recuperar dados para objetos de dispositivo. Essa é a principal diferença entre um manipulador de folha de propriedades normal e um manipulador de folha de propriedades WPD. O código de exemplo a seguir demonstra a recuperação de conteúdo do lado do dispositivo usando a API Windows Shell.

A primeira etapa é a inicialização da lista de identificadores de item ou PIDL. (Esta lista contém o identificador exclusivo para o objeto de dispositivo determinado.)


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



A função de inicialização chama a função ExaminePIDLArray, que recupera as propriedades do objeto identificado por \_ um PIDL na matriz PIDL.


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



Além da inicialização e processamento da lista de identificadores de item, seu aplicativo precisará implementar o método IShellPropSheetExt::ReplacePage e inserir os manipuladores de substituição apropriados. O Windows Shell chama esse método sempre que ele está prestes a exibir uma folha de propriedades substituível, dando ao aplicativo a oportunidade de invocar um manipulador de substituição correspondente. A palavra baixa do primeiro parâmetro para o método ReplacePage é um identificador para a folha de propriedades Windows está prestes a ser exibida. Os valores passados na palavra baixa do primeiro parâmetro correspondem aos valores definidos no arquivo WpdShellExtension.h. Esses valores e suas descrições aparecem na tabela a seguir.



| Valor                                  | Descrição                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ DEVICE \_ GENERAL     | Corresponde à guia geral do dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ STORAGE \_ GENERAL    | Corresponde à guia geral para um objeto de armazenamento encontrado no dispositivo.    |
| CONTEÚDO GERAL DO WPDNSE \_ PROPSHEET \_ \_    | Corresponde à guia geral para o objeto de conteúdo encontrado no dispositivo.      |
| REFERÊNCIAS DE CONTEÚDO DO WPDNSE \_ PROPSHEET \_ \_ | Corresponde à guia referências de um objeto de conteúdo encontrado no dispositivo. |
| RECURSOS DE CONTEÚDO DO WPDNSE \_ PROPSHEET \_ \_  | Corresponde à guia recursos de um objeto de conteúdo encontrado no dispositivo.  |
| DETALHES DO CONTEÚDO DO WPDNSE \_ PROPSHEET \_ \_    | Corresponde a uma guia de detalhes para um objeto de conteúdo encontrado no dispositivo.      |



 

Na extensão de folha de propriedades de exemplo, o método ReplacePage invoca dois manipuladores de substituição: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences. Esses manipuladores substituem o dispositivo geral e as guias de referências de conteúdo nas folhas de propriedades extensíveis.


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



Como é possível que um usuário selecione vários dispositivos, um aplicativo precisará salvar a matriz PIDL retornada por IShellExtInit::Initialize e, em seguida, examinar a palavra alta do primeiro parâmetro para ReplacePage. Um valor de zero nessa palavra alta corresponde ao primeiro elemento na matriz PIDL, um valor de um corresponde ao segundo elemento e assim por diante. Na função ReplacePage do aplicativo de exemplo, esse valor de palavra alta é passado para ambos os manipuladores de substituição. Esses manipuladores, por sua vez, usam esse valor para identificar um dispositivo específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



