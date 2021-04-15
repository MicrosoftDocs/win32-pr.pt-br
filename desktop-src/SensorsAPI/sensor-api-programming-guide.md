---
description: Esta seção fornece informações, incluindo código de exemplo, sobre como usar os recursos de API do sensor. Para obter informações básicas sobre as várias interfaces de programação, consulte sobre a API do sensor.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Guia de programação da API do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078cc99e88a1a4fd6a232220e08c53a99dfbdfb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753924"
---
# <a name="sensor-api-programming-guide"></a><span data-ttu-id="1201a-104">Guia de programação da API do sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-104">Sensor API Programming Guide</span></span>

<span data-ttu-id="1201a-105">Esta seção fornece informações, incluindo código de exemplo, sobre como usar os recursos de API do sensor.</span><span class="sxs-lookup"><span data-stu-id="1201a-105">This section provides information, including example code, about how to use the Sensor API features.</span></span> <span data-ttu-id="1201a-106">Para obter informações básicas sobre as várias interfaces de programação, consulte [sobre a API do sensor](about-the-sensor-api.md).</span><span class="sxs-lookup"><span data-stu-id="1201a-106">For background information about the various programming interfaces, see [About the Sensor API](about-the-sensor-api.md).</span></span>

<span data-ttu-id="1201a-107">O código de exemplo nesta seção utiliza os seguintes cabeçalhos incluídos adicionais.</span><span class="sxs-lookup"><span data-stu-id="1201a-107">The example code in this section makes use of the following additional included headers.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





<span data-ttu-id="1201a-108">Você também deve vincular a esses arquivos de biblioteca associados adicionais: propsys. lib e PortableDeviceGuids. lib.</span><span class="sxs-lookup"><span data-stu-id="1201a-108">You must also link to these additional associated library files: Propsys.lib and PortableDeviceGuids.lib.</span></span>

<span data-ttu-id="1201a-109">O código de exemplo nesta seção usa as seguintes constantes para categorias de sensor, tipos e campos de dados.</span><span class="sxs-lookup"><span data-stu-id="1201a-109">The example code in this section uses the following constants for sensor categories, types, and data fields.</span></span> <span data-ttu-id="1201a-110">Essas constantes são valores personalizados que são definidos pelo exemplo de driver timesensor no kit de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="1201a-110">These constants are custom values that are defined by the TimeSensor driver sample in the Windows Driver Kit.</span></span> <span data-ttu-id="1201a-111">Observe que, embora a plataforma do sensor habilite a definição e o uso de tipos personalizados como esses, você deve usar tipos definidos pela plataforma sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="1201a-111">Note that, though the Sensor platform enables defining and using custom types such as these, you should use platform-defined types whenever possible.</span></span>


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



<span data-ttu-id="1201a-112">O código de exemplo nesta seção usa as seguintes variáveis.</span><span class="sxs-lookup"><span data-stu-id="1201a-112">The example code in this section uses the following variables.</span></span>


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



<span data-ttu-id="1201a-113">O código de exemplo nesta seção usa a seguinte função para liberar ponteiros de interface COM.</span><span class="sxs-lookup"><span data-stu-id="1201a-113">The example code in this section uses the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a><span data-ttu-id="1201a-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1201a-114">In This Section</span></span>

-   [<span data-ttu-id="1201a-115">Recuperando um objeto de sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-115">Retrieving a Sensor Object</span></span>](retrieving-a-sensor.md)
-   [<span data-ttu-id="1201a-116">Solicitando permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="1201a-116">Requesting User Permissions</span></span>](requesting-user-permissions.md)
-   [<span data-ttu-id="1201a-117">Recuperando e definindo propriedades do sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-117">Retrieving and Setting Sensor Properties</span></span>](setting-and-retrieving-sensor-properties.md)
-   [<span data-ttu-id="1201a-118">Verificando os campos de dados de sensor com suporte</span><span class="sxs-lookup"><span data-stu-id="1201a-118">Checking for Supported Sensor Data Fields</span></span>](checking-for-supported-sensor-data-fields.md)
-   [<span data-ttu-id="1201a-119">Usando eventos de API do sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-119">Using Sensor API Events</span></span>](using-sensor-api-events.md)
-   [<span data-ttu-id="1201a-120">Recuperando valores de dados de sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-120">Retrieving Sensor Data Values</span></span>](retrieving-sensor-data-fields.md)
-   [<span data-ttu-id="1201a-121">Recuperando tipos de vetor</span><span class="sxs-lookup"><span data-stu-id="1201a-121">Retrieving Vector Types</span></span>](retrieving-vector-types.md)
-   [<span data-ttu-id="1201a-122">Usando sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="1201a-122">Using Logical Sensors</span></span>](using-logical-sensors.md)
-   [<span data-ttu-id="1201a-123">Criando Light-Aware interfaces de usuário</span><span class="sxs-lookup"><span data-stu-id="1201a-123">Creating Light-Aware User Interfaces</span></span>](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="1201a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1201a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1201a-125">Sobre a API do sensor</span><span class="sxs-lookup"><span data-stu-id="1201a-125">About the Sensor API</span></span>](about-the-sensor-api.md)
</dt> </dl>

 

 



