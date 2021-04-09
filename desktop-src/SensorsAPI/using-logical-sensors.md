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
# <a name="using-logical-sensors"></a>Usando sensores lógicos

Para criar uma instância de um nó de dispositivo para um sensor lógico ou para se reconectar a um nó de dispositivo de sensor lógico existente, um aplicativo ou serviço deve chamar [**ILogicalSensorManager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)). O parâmetro *pPropertyStore* para esse método requer um ponteiro para uma interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que contém as IDs dos drivers do sensor aos quais se conectar. Isso significa que você deve criar um repositório de propriedades e adicionar esses dados ao repositório antes de chamar esse método.

### <a name="connecting-to-the-logical-sensor"></a>Conectando-se ao sensor lógico

Para se conectar a um sensor lógico, você deve fornecer, no mínimo, uma ID de hardware, conforme definido no arquivo. inf do driver do sensor e um **GUID** lógico que identifica o sensor. A plataforma usa esse **GUID** para identificar o sensor quando você opta por desconectar ou desinstalar o nó do dispositivo do sensor.

O código de exemplo a seguir cria um método auxiliar que se conecta a um sensor lógico especificado. Os parâmetros do método recebem a ID de hardware do sensor e um **GUID** exclusivo para identificar o sensor.


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



### <a name="disconnecting-from-a-logical-sensor"></a>Desconectando de um sensor lógico

Para se desconectar de um sensor lógico, você deve fornecer a mesma ID lógica que usou quando chamou [**conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

O código de exemplo a seguir cria uma função auxiliar que se desconecta de um sensor lógico.


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



### <a name="uninstalling-a-logical-sensor"></a>Desinstalando um sensor lógico

Para desinstalar um sensor lógico, você deve fornecer a mesma ID lógica que usou quando chamou [**conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

O código de exemplo a seguir cria uma função auxiliar que desinstala um sensor lógico.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre sensores lógicos](about-logical-sensors.md)
</dt> </dl>

 

 
