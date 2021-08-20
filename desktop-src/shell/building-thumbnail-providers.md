---
description: A partir Windows Vista, maior uso é feito de imagens em miniatura específicas do arquivo do que em versões anteriores do Windows.
title: Criando manipuladores de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4923c01b0387069a8d50ae4d293c40db496f126fdb40ca37d1309dc0201cd51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050853"
---
# <a name="building-thumbnail-handlers"></a>Criando manipuladores de miniaturas

A partir Windows Vista, maior uso é feito de imagens em miniatura específicas do arquivo do que em versões anteriores do Windows. Eles são usados em todas as exibições, em caixas de diálogo e em qualquer tipo de arquivo que as fornece. A exibição em miniatura também foi alterada. Um espectro contínuo de tamanhos selecionáveis pelo usuário está disponível em vez dos tamanhos discretos, como Ícones e Miniaturas.

A interface [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) torna o fornecimento de uma miniatura mais simples do que o [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) ou [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2)mais antigo. Observe, no entanto, que o código existente que usa **IExtractImage** ou **IExtractImage2** ainda é válido e tem suporte.

## <a name="the-recipethumbnailprovider-sample"></a>A amostra RecipeThumbnailProvider

O exemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) dissecado nesta seção está incluído no SDK (Software Development Kit) do Windows. Seu local de instalação padrão é C: Arquivos de \\ \\ Programas Microsoft SDKs \\ Windows \\ v6.0 Exemplos do \\ \\ WinUI Shell \\ \\ AppShellIntegration \\ RecipeThumbnailProvider. No entanto, a maior parte do código também está incluída aqui.

O [exemplo RecipeThumbnailProvider](samples-recipethumbnailprovider.md) demonstra a implementação de um manipulador de miniaturas para um novo tipo de arquivo registrado com uma extensão .recipe. O exemplo ilustra o uso das diferentes AP Component Object Model Is do manipulador de miniaturas para registrar servidores COM (extração de miniaturas) para tipos de arquivo personalizados. Este tópico orienta você pelo código de exemplo, realçando as diretrizes e opções de codificação.

Um manipulador de miniaturas sempre deve implementar [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) em conjunto com uma destas interfaces:

-   [**Iinitializewithstream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**Iinitializewithfile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Há casos em que a inicialização com fluxos não é possível. Em cenários em que o manipulador de miniaturas não implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), ele deve não ser executado no processo isolado em que o indexador do sistema o coloca por padrão quando há uma alteração no fluxo. Para não participar do recurso de isolamento do processo, de definir o valor do Registro a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Se você implementar [**IInitializeWithStream e**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) realizar uma inicialização baseada em fluxo, seu manipulador será mais seguro e confiável. Normalmente, desabilitar o isolamento do processo destina-se apenas a manipuladores herdado; evite desabilitar esse recurso para qualquer novo código. **IInitializeWithStream deve** ser sua primeira opção de interface de inicialização sempre que possível.

Como o arquivo de imagem no exemplo não está inserido no arquivo .recipe e não faz parte de seu fluxo de arquivos, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) é usado no exemplo. A implementação do [**método IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) simplesmente passa seus parâmetros para variáveis de classe privada.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) tem apenas um método,[**GetThumbnail,**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)que é chamado com o maior tamanho desejado da imagem, em pixels. Embora o parâmetro seja chamado *cx*, seu valor é usado como o tamanho máximo das dimensões x e y da imagem. Se a miniatura recuperada não for quadrada, o eixo mais longo será limitado por *cx* e a taxa de proporção da imagem original será preservada.

Quando retorna, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) fornece um handle para a imagem recuperada. Ele também fornece um valor que indica o formato de cor da imagem e se ela tem informações alfa válidas.

A implementação de GetThumbnail no exemplo começa com uma chamada para o método **\_ GetBase64EncodedImageString** privado.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



O tipo de arquivo .recipe é simplesmente um arquivo XML registrado como uma extensão de nome de arquivo exclusiva. Ele inclui um elemento chamado **Picture** que fornece o caminho relativo e o nome de arquivo da imagem a ser usado como a miniatura para esse arquivo .recipe específico. O **elemento Picture** consiste no atributo **Source** que especifica uma imagem codificada em base 64 e um atributo **Size** opcional.

**Size** tem dois valores, Pequeno e Grande. Isso permite que você forneça vários **nós picture** com imagens separadas. A imagem recuperada depende do valor de tamanho máximo (*cx*) fornecido na chamada para [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Como Windows o tamanho da imagem é maior do que seu tamanho máximo, imagens diferentes podem ser fornecidas para resoluções diferentes. No entanto, para simplificar, o exemplo omite o atributo **Size** e fornece apenas uma imagem para todas as situações.

O **\_ método GetBase64EncodedImageString,** cuja implementação é mostrada aqui, usa APIs DOM (xml Modelo de Objeto do Documento) para recuperar o **nó Picture.** Desse nó, ele extrai a imagem dos dados **do atributo Source.**


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



[**GetThumbnail passa**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) a cadeia de caracteres recuperada para **\_ GetStreamFromString.**


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



O **\_ método GetStreamFromString,** cuja implementação é mostrada aqui, que converte a imagem codificada em um fluxo.


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



**Em seguida, GetThumbnail** usa Windows APIs WIC (Componente de Imagem) para extrair um bitmap do fluxo e obter um handle para esse bitmap. As informações alfa são definidas, o WIC é encerrado corretamente e o método é encerrado com êxito.


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

[Manipuladores de miniaturas](thumbnail-providers.md)
</dt> <dt>

[Diretrizes do manipulador de miniaturas](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV \_ ARGS**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
