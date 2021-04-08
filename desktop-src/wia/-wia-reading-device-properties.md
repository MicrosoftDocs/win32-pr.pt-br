---
description: Os aplicativos usam a interface IWiaPropertyStorage de um dispositivo para ler e gravar propriedades de dispositivo. IWiaPropertyStorage herda todos os métodos da interface de Component Object Model (COM) IPropertyStorage.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lendo propriedades do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920946"
---
# <a name="reading-device-properties"></a><span data-ttu-id="d095d-104">Lendo propriedades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d095d-104">Reading Device Properties</span></span>

<span data-ttu-id="d095d-105">Os aplicativos usam a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de um dispositivo para ler e gravar propriedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d095d-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="d095d-106">**IWiaPropertyStorage** herda todos os métodos da interface de Component Object Model (com) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span><span class="sxs-lookup"><span data-stu-id="d095d-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="d095d-107">As propriedades do dispositivo incluem informações sobre um dispositivo que descrevem os recursos e as configurações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d095d-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="d095d-108">Para obter uma lista dessas propriedades, consulte [Propriedades do dispositivo](-wia-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d095d-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="d095d-109">Entre as propriedades do dispositivo que são lidas usando [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) é a ID do dispositivo, que é usada para criar um dispositivo de aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="d095d-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="d095d-110">Para obter mais informações, consulte [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (ou [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span><span class="sxs-lookup"><span data-stu-id="d095d-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="d095d-111">O exemplo a seguir lê a ID do dispositivo, o nome do dispositivo e a descrição do dispositivo da matriz de propriedades do dispositivo e imprime essas propriedades no console do.</span><span class="sxs-lookup"><span data-stu-id="d095d-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


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



<span data-ttu-id="d095d-112">Neste exemplo, o aplicativo configura matrizes [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**PropSpec** e **PropVar**, respectivamente) para manter informações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d095d-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="d095d-113">Essas matrizes são passadas como parâmetros na chamada para o método [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) do ponteiro [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**.</span><span class="sxs-lookup"><span data-stu-id="d095d-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="d095d-114">Cada elemento da matriz **PropSpec** contém o tipo e o nome de uma propriedade de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d095d-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="d095d-115">No retorno, cada elemento de **PropVar** contém o valor da Propriedade do dispositivo representado pelo elemento correspondente da matriz **PropSpec** .</span><span class="sxs-lookup"><span data-stu-id="d095d-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="d095d-116">Em seguida, o aplicativo chama a propriedade [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) do ponteiro [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pWiaPropertyStorage** para recuperar as informações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d095d-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="d095d-117">A técnica usada para ler e definir as propriedades do dispositivo é a mesma das propriedades do item, a única diferença é o tipo do item WIA no qual você chama os métodos apropriados.</span><span class="sxs-lookup"><span data-stu-id="d095d-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="d095d-118">Para obter uma lista de propriedades de item, consulte [Propriedades do item](-wia-item-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d095d-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 
