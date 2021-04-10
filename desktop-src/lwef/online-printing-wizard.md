---
title: Assistente de impressão online
description: O assistente de impressão online do Windows Vista ajuda os usuários a encomendar impressões de fotos de varejistas de impressão online participantes.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Assistente de impressão online
- ícones, assistente de impressão online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294046"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="e8160-105">Assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-105">Online Printing Wizard</span></span>

<span data-ttu-id="e8160-106">O assistente de impressão online do Windows Vista ajuda os usuários a encomendar impressões de fotos de varejistas de impressão online participantes.</span><span class="sxs-lookup"><span data-stu-id="e8160-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="e8160-107">Esse assistente foi projetado para que ele possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de encomendar impressões de fotos.</span><span class="sxs-lookup"><span data-stu-id="e8160-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="e8160-108">O assistente de impressão de fotos está disponível no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8160-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="e8160-109">PIX para Windows</span><span class="sxs-lookup"><span data-stu-id="e8160-109">PIX for Windows</span></span>

-   [<span data-ttu-id="e8160-110">Recursos fornecidos pelo assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="e8160-111">Formatos de arquivo de fotos com suporte</span><span class="sxs-lookup"><span data-stu-id="e8160-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="e8160-112">Iniciando programaticamente o assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="e8160-113">Acessando o ícone do assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="e8160-114">Propriedades MRU do assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="e8160-115">Recursos fornecidos pelo assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="e8160-116">O assistente de impressão online do Windows Vista permite que os usuários solicitem impressões de uma seleção de revendedores de impressão online participante.</span><span class="sxs-lookup"><span data-stu-id="e8160-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="e8160-117">Quando invocado, o assistente:</span><span class="sxs-lookup"><span data-stu-id="e8160-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="e8160-118">Aceita um arquivo ou lista de arquivos para os quais as impressões devem ser ordenadas.</span><span class="sxs-lookup"><span data-stu-id="e8160-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="e8160-119">Recupera automaticamente a lista atual de varejistas de impressão online participantes e permite que o usuário selecione o varejista do qual comprar as impressões de fotos.</span><span class="sxs-lookup"><span data-stu-id="e8160-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="e8160-120">Orienta o usuário pelo processo ou pelo pedido de impressões.</span><span class="sxs-lookup"><span data-stu-id="e8160-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="e8160-121">Qualquer aplicativo pode se beneficiar dos recursos oferecidos pelo assistente de impressão online do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8160-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="e8160-122">Um aplicativo precisa apenas passar o arquivo ou arquivos para os quais as impressões serão ordenadas e o assistente orientará o usuário por meio do processo de ordenação.</span><span class="sxs-lookup"><span data-stu-id="e8160-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="e8160-123">A figura a seguir mostra o assistente de impressão online do Windows Vista exibindo uma lista de exemplos de varejistas de impressão online participantes.</span><span class="sxs-lookup"><span data-stu-id="e8160-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![o assistente de impressão online do Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="e8160-125">Formatos de arquivo de fotos com suporte</span><span class="sxs-lookup"><span data-stu-id="e8160-125">Supported Photo File Formats</span></span>

<span data-ttu-id="e8160-126">O assistente de impressão online do Windows Vista oferece suporte a qualquer formato de arquivo de imagem para o qual um codec do Windows Imaging Component (WIC) esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="e8160-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="e8160-127">O WIC fornece vários codecs padrão, incluindo:</span><span class="sxs-lookup"><span data-stu-id="e8160-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="e8160-128">BMP (Bitmap)</span><span class="sxs-lookup"><span data-stu-id="e8160-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="e8160-129">GIF</span><span class="sxs-lookup"><span data-stu-id="e8160-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="e8160-130">Formato de ícone (ICO)</span><span class="sxs-lookup"><span data-stu-id="e8160-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="e8160-131">JPEG</span><span class="sxs-lookup"><span data-stu-id="e8160-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="e8160-132">PNG</span><span class="sxs-lookup"><span data-stu-id="e8160-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="e8160-133">TIFF</span><span class="sxs-lookup"><span data-stu-id="e8160-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="e8160-134">Formato de foto do Windows Media</span><span class="sxs-lookup"><span data-stu-id="e8160-134">Windows Media Photo format</span></span>

<span data-ttu-id="e8160-135">Para obter mais informações sobre os codecs WIC e WIC, consulte [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="e8160-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="e8160-136">Os formatos de arquivo com suporte de revendedores de impressão online variam de varejista para varejista; é possível que um varejista específico não ofereça suporte a todos os formatos de arquivo suportados pelo assistente de impressão online do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8160-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="e8160-137">Se o usuário tentar solicitar impressões em um formato que não tenha suporte do varejista selecionado, o assistente de impressão online do Windows Vista notificará o usuário de que o varejista selecionado não oferece suporte ao formato de arquivo enviado.</span><span class="sxs-lookup"><span data-stu-id="e8160-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="e8160-138">Iniciando programaticamente o assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="e8160-139">Para invocar o assistente de impressão online do Windows Vista, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte CLSID (identificador de classe):</span><span class="sxs-lookup"><span data-stu-id="e8160-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="e8160-140">Esse CLSID é definido em ShObjIdl. h e ShObjIdl. idl.</span><span class="sxs-lookup"><span data-stu-id="e8160-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="e8160-141">Os arquivos a serem processados pelo assistente de impressão online do Windows Vista são especificados em um objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="e8160-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="e8160-142">O exemplo de código a seguir demonstra como invocar o assistente de impressão online do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8160-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="e8160-143">Acessando o ícone do assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="e8160-144">O assistente de impressão online do Windows Vista exporta um ícone que pode ser acessado e exibido por aplicativos que o chamam.</span><span class="sxs-lookup"><span data-stu-id="e8160-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="e8160-145">A figura a seguir mostra o ícone do assistente de impressão online do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8160-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![o ícone do assistente de impressão online do Windows Vista](images/opw-icon.png)

<span data-ttu-id="e8160-147">O exemplo de código a seguir demonstra como recuperar o índice para o ícone do assistente de impressão online do Windows Vista lendo a propriedade **OPWIcon** .</span><span class="sxs-lookup"><span data-stu-id="e8160-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="e8160-148">Propriedades MRU do assistente de impressão online</span><span class="sxs-lookup"><span data-stu-id="e8160-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="e8160-149">O assistente de impressão online do Windows Vista define três propriedades que estão relacionadas ao varejista de impressão online usado mais recentemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="e8160-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="e8160-150">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="e8160-150">Property Name</span></span> | <span data-ttu-id="e8160-151">Valor/função da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8160-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8160-152">**MRUIcon**</span><span class="sxs-lookup"><span data-stu-id="e8160-152">**MRUIcon**</span></span>   | <span data-ttu-id="e8160-153">O índice do ícone para o varejista de impressão online usado mais recentemente pode ser lido com base nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="e8160-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="e8160-154">**MRUName**</span><span class="sxs-lookup"><span data-stu-id="e8160-154">**MRUName**</span></span>   | <span data-ttu-id="e8160-155">O nome do varejista de impressão online usado mais recentemente pode ser lido com base nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="e8160-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="e8160-156">**UseMRU**</span><span class="sxs-lookup"><span data-stu-id="e8160-156">**UseMRU**</span></span>    | <span data-ttu-id="e8160-157">Um valor  \*\* \_ booliano\*\* de **Variant** VT que indica se o assistente deve ignorar a página de seleção de revendedor de impressão online e apenas usar o revendedor de impressão online usado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="e8160-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="e8160-158">Defina essa propriedade como **Variant \_ true** para ignorar a página de seleção de varejista.</span><span class="sxs-lookup"><span data-stu-id="e8160-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="e8160-159">O exemplo de código a seguir demonstra como definir a propriedade UseMRU para que o assistente de impressão online do Windows Vista ignore a página de seleção de revendedor de impressão online e selecione automaticamente o varejista usado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="e8160-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="e8160-160">O exemplo de código a seguir demonstra como ler as propriedades MRUName e MRUIcon.</span><span class="sxs-lookup"><span data-stu-id="e8160-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 