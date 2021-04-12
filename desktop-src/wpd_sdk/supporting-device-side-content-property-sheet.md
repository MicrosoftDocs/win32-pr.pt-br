---
title: Suporte ao conteúdo do lado do dispositivo (folha)
description: Suporte a conteúdo Device-Side
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297132"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="66877-103">Suporte ao conteúdo do lado do dispositivo</span><span class="sxs-lookup"><span data-stu-id="66877-103">Supporting device-side content</span></span>

<span data-ttu-id="66877-104">Como o conteúdo do lado do dispositivo não é acessível por meio do sistema de arquivos no Windows Vista, você precisará usar a API do shell do Windows ou a API WPD para recuperar dados de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="66877-105">Essa é a principal diferença entre um manipulador de folhas de propriedades normal e um manipulador de folhas de propriedades WPD.</span><span class="sxs-lookup"><span data-stu-id="66877-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="66877-106">O código de exemplo a seguir demonstra a recuperação do conteúdo do lado do dispositivo usando a API do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="66877-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="66877-107">A primeira etapa é a inicialização da lista de identificadores de item ou PIDL.</span><span class="sxs-lookup"><span data-stu-id="66877-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="66877-108">(Essa lista contém o identificador exclusivo para o objeto de dispositivo fornecido.)</span><span class="sxs-lookup"><span data-stu-id="66877-108">(This list contains the unique identifier for the given device object.)</span></span>


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



<span data-ttu-id="66877-109">A função de inicialização chama a \_ função ExaminePIDLArray, que recupera as propriedades do objeto identificado por um PIDL na matriz PIDL.</span><span class="sxs-lookup"><span data-stu-id="66877-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


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



<span data-ttu-id="66877-110">Além da inicialização e do processamento da lista de identificadores de item, seu aplicativo precisará implementar o método IShellPropSheetExt:: ReplacePage e inserir os manipuladores de substituição apropriados.</span><span class="sxs-lookup"><span data-stu-id="66877-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="66877-111">O Shell do Windows chama esse método cada vez que está prestes a exibir uma folha de propriedades substituível, dando ao seu aplicativo uma chance de invocar um manipulador de substituição correspondente.</span><span class="sxs-lookup"><span data-stu-id="66877-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="66877-112">A palavra baixa do primeiro parâmetro para o método ReplacePage é um identificador para a folha de propriedades fornecida que o Windows está prestes a exibir.</span><span class="sxs-lookup"><span data-stu-id="66877-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="66877-113">Os valores passados na palavra inferior do primeiro parâmetro correspondem aos valores definidos no arquivo WpdShellExtension. h.</span><span class="sxs-lookup"><span data-stu-id="66877-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="66877-114">Esses valores e suas descrições aparecem na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="66877-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="66877-115">Valor</span><span class="sxs-lookup"><span data-stu-id="66877-115">Value</span></span>                                  | <span data-ttu-id="66877-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="66877-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="66877-117">WPDNSE \_ PROPSHEET \_ dispositivo \_ geral</span><span class="sxs-lookup"><span data-stu-id="66877-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="66877-118">Corresponde à guia Geral do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="66877-119">WPDNSE \_ PROPSHEET \_ armazenamento \_ geral</span><span class="sxs-lookup"><span data-stu-id="66877-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="66877-120">Corresponde à guia geral de um objeto de armazenamento encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="66877-121">\_ \_ conteúdo \_ geral do WPDNSE PROPSHEET</span><span class="sxs-lookup"><span data-stu-id="66877-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="66877-122">Corresponde à guia Geral do objeto de conteúdo encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="66877-123">WPDNSE \_ PROPSHEET \_ referências de conteúdo \_</span><span class="sxs-lookup"><span data-stu-id="66877-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="66877-124">Corresponde à guia References de um objeto de conteúdo encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="66877-125">recursos de conteúdo do WPDNSE \_ PROPSHEET \_ \_</span><span class="sxs-lookup"><span data-stu-id="66877-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="66877-126">Corresponde à guia de recursos de um objeto de conteúdo encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="66877-127">detalhes do conteúdo do WPDNSE \_ PROPSHEET \_ \_</span><span class="sxs-lookup"><span data-stu-id="66877-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="66877-128">Corresponde a uma guia de detalhes de um objeto de conteúdo encontrado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66877-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="66877-129">Na extensão da folha de propriedades de exemplo, o método ReplacePage invoca dois manipuladores de substituição: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences.</span><span class="sxs-lookup"><span data-stu-id="66877-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="66877-130">Esses manipuladores substituem as guias dispositivo geral e referências de conteúdo nas folhas de propriedades extensível.</span><span class="sxs-lookup"><span data-stu-id="66877-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


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



<span data-ttu-id="66877-131">Como é possível que um usuário Selecione vários dispositivos, um aplicativo precisará salvar a matriz PIDL retornada por IShellExtInit:: Initialize e, em seguida, examinar a palavra alta do primeiro parâmetro para ReplacePage.</span><span class="sxs-lookup"><span data-stu-id="66877-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="66877-132">Um valor igual a zero nesta palavra alta corresponde ao primeiro elemento na matriz PIDL, um valor de um corresponde ao segundo elemento e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="66877-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="66877-133">Na função ReplacePage do aplicativo de exemplo, esse valor de palavra alta é passado para ambos os manipuladores de substituição.</span><span class="sxs-lookup"><span data-stu-id="66877-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="66877-134">Esses manipuladores, por sua vez, usam esse valor para identificar um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="66877-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66877-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66877-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66877-136">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="66877-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



