---
description: Usando sensores lógicos
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Usando sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090165"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="58af3-103">Usando sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="58af3-103">Using Logical Sensors</span></span>

<span data-ttu-id="58af3-104">Para criar uma instância de um nó de dispositivo para um sensor lógico ou para se reconectar a um nó de dispositivo de sensor lógico existente, um aplicativo ou serviço deve chamar [**ILogicalSensorManager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58af3-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="58af3-105">O parâmetro *pPropertyStore* para esse método requer um ponteiro para uma interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que contém as IDs dos drivers do sensor aos quais se conectar.</span><span class="sxs-lookup"><span data-stu-id="58af3-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="58af3-106">Isso significa que você deve criar um repositório de propriedades e adicionar esses dados ao repositório antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="58af3-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="58af3-107">Conectando-se ao sensor lógico</span><span class="sxs-lookup"><span data-stu-id="58af3-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="58af3-108">Para se conectar a um sensor lógico, você deve fornecer, no mínimo, uma ID de hardware, conforme definido no arquivo. inf do driver do sensor e um **GUID** lógico que identifica o sensor.</span><span class="sxs-lookup"><span data-stu-id="58af3-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="58af3-109">A plataforma usa esse **GUID** para identificar o sensor quando você opta por desconectar ou desinstalar o nó do dispositivo do sensor.</span><span class="sxs-lookup"><span data-stu-id="58af3-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="58af3-110">O código de exemplo a seguir cria um método auxiliar que se conecta a um sensor lógico especificado.</span><span class="sxs-lookup"><span data-stu-id="58af3-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="58af3-111">Os parâmetros do método recebem a ID de hardware do sensor e um **GUID** exclusivo para identificar o sensor.</span><span class="sxs-lookup"><span data-stu-id="58af3-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="58af3-112">Desconectando de um sensor lógico</span><span class="sxs-lookup"><span data-stu-id="58af3-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="58af3-113">Para se desconectar de um sensor lógico, você deve fornecer a mesma ID lógica que usou quando chamou [**conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58af3-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="58af3-114">O código de exemplo a seguir cria uma função auxiliar que se desconecta de um sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="58af3-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="58af3-115">Desinstalando um sensor lógico</span><span class="sxs-lookup"><span data-stu-id="58af3-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="58af3-116">Para desinstalar um sensor lógico, você deve fornecer a mesma ID lógica que usou quando chamou [**conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58af3-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="58af3-117">O código de exemplo a seguir cria uma função auxiliar que desinstala um sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="58af3-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="58af3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58af3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58af3-119">Sobre sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="58af3-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
