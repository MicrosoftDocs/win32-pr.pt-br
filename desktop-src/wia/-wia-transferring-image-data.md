---
description: Use os métodos da interface IWiaDataTransfer para transferir dados de um dispositivo de aquisição de imagem do Windows (WIA) 1,0 para um aplicativo.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Transferindo dados de imagem no WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090494"
---
# <a name="transferring-image-data-in-wia-10"></a>Transferindo dados de imagem no WIA 1,0

> [!Note]  
> Este tutorial é sobre a transferência de dados de imagem em aplicativos que executarão o Windows XP ou anterior. Consulte [transferindo dados de imagem no WIA 2,0](-wia-transferring-image-data-in-wia2.md) para obter informações sobre como transferir dados de imagem em aplicativos que serão executados no Windows Vista ou posterior.

 

Use os métodos da interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) para transferir dados de um dispositivo de aquisição de imagem do Windows (WIA) 1,0 para um aplicativo. Essa interface dá suporte a uma janela de memória compartilhada para transferir dados do objeto de dispositivo para o aplicativo e eliminar cópias de dados desnecessárias durante o marshaling.

Os aplicativos devem consultar um item de imagem para obter um ponteiro para sua interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , como no exemplo de código a seguir:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



No código anterior, supõe-se que **pWiaItem** é um ponteiro válido para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . A chamada para [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) preenche **pWiaDataTransfer** com um ponteiro para a interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) do item referido por **pWiaItem**.

Em seguida, o aplicativo define os membros da estrutura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Para obter informações, consulte STGMEDIUM e [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Se você fornecer um FileName, ele deverá incluir a extensão de arquivo apropriada; O WIA 1,0 não fornece extensões de arquivo. Se o membro **lpszFileName** de **StgMedium** for **NULL**, o WIA 1,0 gerará um nome de arquivo aleatório e um caminho para os dados transferidos. Mova ou copie esse arquivo antes de chamar ReleaseStgMedium, pois essa função excluirá o arquivo.

Em seguida, o aplicativo chama o método [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) para executar a transferência de dados:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



Na chamada para [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), o segundo parâmetro especifica um ponteiro para a interface [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) . Os aplicativos devem implementar essa interface para receber retornos de chamada durante transferências de dados. Para obter informações sobre como implementar essa interface, consulte [**IWiaDataCallback:: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

Em seguida, o aplicativo libera os ponteiros para a interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) e libera todos os dados alocados na estrutura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

O aplicativo também pode transferir a imagem usando transferências de dados na memória em vez de transferências de arquivo. Nesse caso, o aplicativo usa o método idtGetBandedData no lugar do método idtGetData.

Aqui está o exemplo completo de transferência de dados:


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
