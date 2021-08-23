---
description: Como a transferência de dados de imagem é baseada em fluxo no WIA (Aquisição de Imagem) 2.0 do Windows, você não precisa especificar um tipo de destino (por exemplo,
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Transferindo dados de imagem no WIA 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66aca2179c477f49bc76197795ddf9d59792ca242da8729c169c39aa69553161
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592956"
---
# <a name="transferring-image-data-in-wia-20"></a>Transferindo dados de imagem no WIA 2.0

> [!Note]  
> Este tutorial demonstra como transferir dados de imagem em aplicativos executados no Windows Vista ou posterior. Consulte Transferindo dados de imagem no [WIA 1.0](-wia-transferring-image-data.md) para obter informações sobre como transferir dados de imagem em aplicativos executados no Windows XP ou anterior.

 

Como a transferência de dados de imagem é baseada em fluxo no WIA (Aquisição de Imagem) 2.0 do Windows, você não precisa especificar um tipo de destino (por exemplo, memória ou arquivo). O aplicativo simplesmente fornece ao WIA 2.0 o fluxo a ser usado e o driver lê ou grava no fluxo. O fluxo pode ser um fluxo de arquivos, um fluxo de memória ou qualquer outro tipo de fluxo e é transparente para o driver. O uso de fluxos também fornece uma integração fácil com o filtro processamento de imagem.

Use os métodos da interface [**IWiaTransfer**](-wia-iwiatransfer.md) para transferir dados de um dispositivo WIA 2.0 para um aplicativo. Essa interface está disponível por meio da interface [**IWiaItem2.**](-wia-iwiaitem2.md) A interface **IWiaTransfer** tem métodos para solicitar o upload ou o download de dados de e para um dispositivo. Esses métodos usam um retorno de chamada fornecido pelo aplicativo e usam um [IStream](/windows/win32/api/objidl/nn-objidl-istream) fornecido pelo aplicativo para o destino real da transferência de dados.

Os aplicativos devem consultar um item de imagem para obter um ponteiro para sua interface [**IWiaTransfer,**](-wia-iwiatransfer.md) conforme mostrado no exemplo de código a seguir:


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



No código anterior, presumimos que **pWiaItem2 é** um ponteiro válido para a interface [**IWiaItem2.**](-wia-iwiaitem2.md) A chamada para [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) preenche **pWiaTransfer** com um ponteiro para a interface [**IWiaTransfer**](-wia-iwiatransfer.md) do item referenciado por **pWiaItem2**.

Em seguida, o aplicativo instalita o objeto de retorno de chamada, conforme mostrado aqui.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



Em seguida, o aplicativo define as propriedades usando a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) do item [**IWiaItem2**](-wia-iwiaitem2.md) e executa a transferência.

Transferindo:


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Upload:


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Aqui está o exemplo completo de transferência de dados:


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
