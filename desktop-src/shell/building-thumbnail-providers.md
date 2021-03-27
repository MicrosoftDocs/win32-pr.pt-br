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
# <a name="building-thumbnail-handlers"></a>Criando manipuladores de miniatura

A partir do Windows Vista, é feita uma maior utilização de imagens em miniaturas específicas de arquivo do que nas versões anteriores do Windows. Eles são usados em todas as exibições, em caixas de diálogo e em qualquer tipo de arquivo que as forneça. A exibição de miniatura também foi alterada. Um espectro contínuo de tamanhos selecionáveis pelo usuário está disponível em vez de tamanhos discretos, como ícones e miniaturas.

A interface [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) facilita o fornecimento de uma miniatura mais simples do que o [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ou o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2)mais antigo. No entanto, observe que o código existente que usa **IExtractImage** ou **IExtractImage2** ainda é válido e tem suporte.

## <a name="the-recipethumbnailprovider-sample"></a>O exemplo de RecipeThumbnailProvider

O exemplo de [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) que foi examinado nesta seção está incluído no SDK (Software Development Kit) do Windows. Seu local de instalação padrão é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ WinUI \\ shell \\ AppShellIntegration \\ RecipeThumbnailProvider. No entanto, a massa do código também é incluída aqui.

O exemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) demonstra a implementação de um manipulador de miniaturas para um novo tipo de arquivo registrado com uma extensão. recipe. O exemplo ilustra o uso das diferentes APIs do manipulador de miniaturas para registrar servidores COM (Component Object Model de extração de miniaturas) para tipos de arquivo personalizados. Este tópico orienta você pelo código de exemplo, destacando as opções e as diretrizes de codificação.

Um manipulador de miniaturas sempre deve implementar [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) em conjunto com uma destas interfaces:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Há casos em que a inicialização com fluxos não é possível. Em cenários em que o seu manipulador de miniaturas não implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), ele deve recusar a execução no processo isolado em que o indexador do sistema o coloca por padrão quando há uma alteração no fluxo. Para recusar o recurso de isolamento de processo, defina o valor do registro a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Se você implementar o [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) e realizar uma inicialização baseada em fluxo, seu manipulador será mais seguro e confiável. Normalmente, desabilitar o isolamento de processo destina-se apenas a manipuladores herdados; Evite desabilitar esse recurso para qualquer código novo. **IInitializeWithStream** deve ser sua primeira opção de interface de inicialização sempre que possível.

Como o arquivo de imagem no exemplo não é inserido no arquivo. recipe e não faz parte de seu fluxo de arquivos, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) é usado no exemplo. A implementação do método [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) simplesmente passa seus parâmetros para variáveis de classe privada.

[**Manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) tem apenas um método —[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)— que é chamado com o maior tamanho desejado da imagem, em pixels. Embora o parâmetro seja denominado *CX*, seu valor é usado como o tamanho máximo das dimensões x e y da imagem. Se a miniatura recuperada não for quadrada, o eixo mais longo será limitado pelo *CX* e a taxa de proporção da imagem original será preservada.

Quando retorna, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornece um identificador para a imagem recuperada. Ele também fornece um valor que indica o formato de cor da imagem e se ele tem informações de alfa válidas.

A implementação GetThumbnail no exemplo começa com uma chamada para o método **\_ GetBase64EncodedImageString** privado.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



O tipo de arquivo. recipe é simplesmente um arquivo XML registrado como uma extensão de nome de arquivo exclusiva. Ele inclui um elemento chamado **Picture** que fornece o caminho relativo e o nome do arquivo da imagem a ser usada como a miniatura desse arquivo. recipe específico. O elemento **Picture** consiste no atributo **Source** que especifica uma imagem codificada base 64 e um atributo de **tamanho** opcional.

O **tamanho** tem dois valores, pequeno e grande. Isso permite que você forneça vários nós de **imagem** com imagens separadas. A imagem recuperada depende do valor de tamanho máximo (*CX*) fornecido na chamada para [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Como o Windows nunca dimensiona a imagem para maior do que seu tamanho máximo, imagens diferentes podem ser fornecidas para diferentes resoluções. No entanto, para simplificar, o exemplo omite o atributo **size** e fornece apenas uma imagem para todas as situações.

O método **\_ GetBase64EncodedImageString** , cuja implementação é mostrada aqui, usa APIs DOM (XML modelo de objeto do documento) para recuperar o nó da **imagem** . A partir desse nó, ele extrai a imagem dos dados de atributo de **origem** .


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



[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) então passa a cadeia de caracteres recuperada para **\_ GetStreamFromString**.


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



O método **\_ GetStreamFromString** , cuja implementação é mostrada aqui, que converte a imagem codificada em um fluxo.


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



Em seguida, **GetThumbnail** usa APIs do Windows Imaging Component (WIC) para extrair um bitmap do fluxo e obter um identificador para esse bitmap. As informações Alfa são definidas, o WIC é encerrado corretamente e o método termina com êxito.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipuladores de miniatura](thumbnail-providers.md)
</dt> <dt>

[Diretrizes do manipulador de miniaturas](thumbnail-provider-guidelines.md)
</dt> <dt>

[**\_argumentos de PPV de IID \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
