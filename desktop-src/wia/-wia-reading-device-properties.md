---
description: Os aplicativos usam a interface IWiaPropertyStorage de um dispositivo para ler e gravar propriedades de dispositivo. IWiaPropertyStorage herda todos os métodos da interface de Component Object Model (COM) IPropertyStorage.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lendo propriedades do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf102fb2ade1a13b648e13f56f7f999dd35c41f721ac20d72914219c98311505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669256"
---
# <a name="reading-device-properties"></a>Lendo propriedades do dispositivo

Os aplicativos usam a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de um dispositivo para ler e gravar propriedades de dispositivo. **IWiaPropertyStorage** herda todos os métodos da interface de Component Object Model (com) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).

As propriedades do dispositivo incluem informações sobre um dispositivo que descrevem os recursos e as configurações do dispositivo. Para obter uma lista dessas propriedades, consulte [Propriedades do dispositivo](-wia-device-properties.md).

entre as propriedades do dispositivo que são lidas usando [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) é a ID do dispositivo, que é usada para criar um dispositivo de aquisição de imagem Windows (WIA). Para obter mais informações, consulte [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).

O exemplo a seguir lê a ID do dispositivo, o nome do dispositivo e a descrição do dispositivo da matriz de propriedades do dispositivo e imprime essas propriedades no console do.


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



Neste exemplo, o aplicativo configura matrizes [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**PropSpec** e **PropVar**, respectivamente) para manter informações de propriedade. Essas matrizes são passadas como parâmetros na chamada para o método [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) do ponteiro [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**. Cada elemento da matriz **PropSpec** contém o tipo e o nome de uma propriedade de dispositivo. No retorno, cada elemento de **PropVar** contém o valor da Propriedade do dispositivo representado pelo elemento correspondente da matriz **PropSpec** .

Em seguida, o aplicativo chama a propriedade [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) do ponteiro [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pWiaPropertyStorage** para recuperar as informações de propriedade.

A técnica usada para ler e definir as propriedades do dispositivo é a mesma das propriedades do item, a única diferença é o tipo do item WIA no qual você chama os métodos apropriados. Para obter uma lista de propriedades de item, consulte [Propriedades do item](-wia-item-properties.md).

 

 
