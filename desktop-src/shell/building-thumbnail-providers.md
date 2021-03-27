---
description: A partir do Windows Vista, é feita uma maior utilização de imagens em miniaturas específicas de arquivo do que nas versões anteriores do Windows.
title: Criando manipuladores de miniatura
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967360"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="3067c-103">Criando manipuladores de miniatura</span><span class="sxs-lookup"><span data-stu-id="3067c-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="3067c-104">A partir do Windows Vista, é feita uma maior utilização de imagens em miniaturas específicas de arquivo do que nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="3067c-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="3067c-105">Eles são usados em todas as exibições, em caixas de diálogo e em qualquer tipo de arquivo que as forneça.</span><span class="sxs-lookup"><span data-stu-id="3067c-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="3067c-106">A exibição de miniatura também foi alterada.</span><span class="sxs-lookup"><span data-stu-id="3067c-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="3067c-107">Um espectro contínuo de tamanhos selecionáveis pelo usuário está disponível em vez de tamanhos discretos, como ícones e miniaturas.</span><span class="sxs-lookup"><span data-stu-id="3067c-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="3067c-108">A interface [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) facilita o fornecimento de uma miniatura mais simples do que o [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ou o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2)mais antigo.</span><span class="sxs-lookup"><span data-stu-id="3067c-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="3067c-109">No entanto, observe que o código existente que usa **IExtractImage** ou **IExtractImage2** ainda é válido e tem suporte.</span><span class="sxs-lookup"><span data-stu-id="3067c-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="3067c-110">O exemplo de RecipeThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="3067c-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="3067c-111">O exemplo de [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) que foi examinado nesta seção está incluído no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="3067c-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3067c-112">Seu local de instalação padrão é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ WinUI \\ shell \\ AppShellIntegration \\ RecipeThumbnailProvider.</span><span class="sxs-lookup"><span data-stu-id="3067c-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="3067c-113">No entanto, a massa do código também é incluída aqui.</span><span class="sxs-lookup"><span data-stu-id="3067c-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="3067c-114">O exemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) demonstra a implementação de um manipulador de miniaturas para um novo tipo de arquivo registrado com uma extensão. recipe.</span><span class="sxs-lookup"><span data-stu-id="3067c-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="3067c-115">O exemplo ilustra o uso das diferentes APIs do manipulador de miniaturas para registrar servidores COM (Component Object Model de extração de miniaturas) para tipos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="3067c-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="3067c-116">Este tópico orienta você pelo código de exemplo, destacando as opções e as diretrizes de codificação.</span><span class="sxs-lookup"><span data-stu-id="3067c-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="3067c-117">Um manipulador de miniaturas sempre deve implementar [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) em conjunto com uma destas interfaces:</span><span class="sxs-lookup"><span data-stu-id="3067c-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="3067c-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="3067c-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="3067c-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="3067c-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="3067c-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="3067c-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="3067c-121">Há casos em que a inicialização com fluxos não é possível.</span><span class="sxs-lookup"><span data-stu-id="3067c-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="3067c-122">Em cenários em que o seu manipulador de miniaturas não implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), ele deve recusar a execução no processo isolado em que o indexador do sistema o coloca por padrão quando há uma alteração no fluxo.</span><span class="sxs-lookup"><span data-stu-id="3067c-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="3067c-123">Para recusar o recurso de isolamento de processo, defina o valor do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="3067c-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="3067c-124">Se você implementar o [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) e realizar uma inicialização baseada em fluxo, seu manipulador será mais seguro e confiável.</span><span class="sxs-lookup"><span data-stu-id="3067c-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="3067c-125">Normalmente, desabilitar o isolamento de processo destina-se apenas a manipuladores herdados; Evite desabilitar esse recurso para qualquer código novo.</span><span class="sxs-lookup"><span data-stu-id="3067c-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="3067c-126">**IInitializeWithStream** deve ser sua primeira opção de interface de inicialização sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="3067c-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="3067c-127">Como o arquivo de imagem no exemplo não é inserido no arquivo. recipe e não faz parte de seu fluxo de arquivos, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) é usado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="3067c-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="3067c-128">A implementação do método [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) simplesmente passa seus parâmetros para variáveis de classe privada.</span><span class="sxs-lookup"><span data-stu-id="3067c-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="3067c-129">[**Manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) tem apenas um método —[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)— que é chamado com o maior tamanho desejado da imagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="3067c-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="3067c-130">Embora o parâmetro seja denominado *CX*, seu valor é usado como o tamanho máximo das dimensões x e y da imagem.</span><span class="sxs-lookup"><span data-stu-id="3067c-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="3067c-131">Se a miniatura recuperada não for quadrada, o eixo mais longo será limitado pelo *CX* e a taxa de proporção da imagem original será preservada.</span><span class="sxs-lookup"><span data-stu-id="3067c-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="3067c-132">Quando retorna, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornece um identificador para a imagem recuperada.</span><span class="sxs-lookup"><span data-stu-id="3067c-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="3067c-133">Ele também fornece um valor que indica o formato de cor da imagem e se ele tem informações de alfa válidas.</span><span class="sxs-lookup"><span data-stu-id="3067c-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="3067c-134">A implementação GetThumbnail no exemplo começa com uma chamada para o método **\_ GetBase64EncodedImageString** privado.</span><span class="sxs-lookup"><span data-stu-id="3067c-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="3067c-135">O tipo de arquivo. recipe é simplesmente um arquivo XML registrado como uma extensão de nome de arquivo exclusiva.</span><span class="sxs-lookup"><span data-stu-id="3067c-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="3067c-136">Ele inclui um elemento chamado **Picture** que fornece o caminho relativo e o nome do arquivo da imagem a ser usada como a miniatura desse arquivo. recipe específico.</span><span class="sxs-lookup"><span data-stu-id="3067c-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="3067c-137">O elemento **Picture** consiste no atributo **Source** que especifica uma imagem codificada base 64 e um atributo de **tamanho** opcional.</span><span class="sxs-lookup"><span data-stu-id="3067c-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="3067c-138">O **tamanho** tem dois valores, pequeno e grande.</span><span class="sxs-lookup"><span data-stu-id="3067c-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="3067c-139">Isso permite que você forneça vários nós de **imagem** com imagens separadas.</span><span class="sxs-lookup"><span data-stu-id="3067c-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="3067c-140">A imagem recuperada depende do valor de tamanho máximo (*CX*) fornecido na chamada para [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span><span class="sxs-lookup"><span data-stu-id="3067c-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="3067c-141">Como o Windows nunca dimensiona a imagem para maior do que seu tamanho máximo, imagens diferentes podem ser fornecidas para diferentes resoluções.</span><span class="sxs-lookup"><span data-stu-id="3067c-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="3067c-142">No entanto, para simplificar, o exemplo omite o atributo **size** e fornece apenas uma imagem para todas as situações.</span><span class="sxs-lookup"><span data-stu-id="3067c-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="3067c-143">O método **\_ GetBase64EncodedImageString** , cuja implementação é mostrada aqui, usa APIs DOM (XML modelo de objeto do documento) para recuperar o nó da **imagem** .</span><span class="sxs-lookup"><span data-stu-id="3067c-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="3067c-144">A partir desse nó, ele extrai a imagem dos dados de atributo de **origem** .</span><span class="sxs-lookup"><span data-stu-id="3067c-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="3067c-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) então passa a cadeia de caracteres recuperada para **\_ GetStreamFromString**.</span><span class="sxs-lookup"><span data-stu-id="3067c-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="3067c-146">O método **\_ GetStreamFromString** , cuja implementação é mostrada aqui, que converte a imagem codificada em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="3067c-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="3067c-147">Em seguida, **GetThumbnail** usa APIs do Windows Imaging Component (WIC) para extrair um bitmap do fluxo e obter um identificador para esse bitmap.</span><span class="sxs-lookup"><span data-stu-id="3067c-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="3067c-148">As informações Alfa são definidas, o WIC é encerrado corretamente e o método termina com êxito.</span><span class="sxs-lookup"><span data-stu-id="3067c-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3067c-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3067c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3067c-150">Manipuladores de miniatura</span><span class="sxs-lookup"><span data-stu-id="3067c-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="3067c-151">Diretrizes do manipulador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="3067c-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="3067c-152">**\_argumentos de PPV de IID \_**</span><span class="sxs-lookup"><span data-stu-id="3067c-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
