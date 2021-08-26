---
description: Esta seção fornece informações, incluindo código de exemplo, sobre como usar os recursos de API do sensor. Para obter informações básicas sobre as várias interfaces de programação, consulte sobre a API do sensor.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Guia de programação da API do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5886564e66a0a8db64713b280b44f85a197430dc23523266bc45e66e44c956b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073236"
---
# <a name="sensor-api-programming-guide"></a>Guia de programação da API do sensor

Esta seção fornece informações, incluindo código de exemplo, sobre como usar os recursos de API do sensor. Para obter informações básicas sobre as várias interfaces de programação, consulte [sobre a API do sensor](about-the-sensor-api.md).

O código de exemplo nesta seção utiliza os seguintes cabeçalhos incluídos adicionais.


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





Você também deve vincular a esses arquivos de biblioteca associados adicionais: propsys. lib e PortableDeviceGuids. lib.

O código de exemplo nesta seção usa as seguintes constantes para categorias de sensor, tipos e campos de dados. essas constantes são valores personalizados que são definidos pelo exemplo de driver timesensor no Kit de driver Windows. Observe que, embora a plataforma do sensor habilite a definição e o uso de tipos personalizados como esses, você deve usar tipos definidos pela plataforma sempre que possível.


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



O código de exemplo nesta seção usa as seguintes variáveis.


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



O código de exemplo nesta seção usa a seguinte função para liberar ponteiros de interface COM.


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



## <a name="in-this-section"></a>Nesta seção

-   [Recuperando um objeto de sensor](retrieving-a-sensor.md)
-   [Solicitando permissões de usuário](requesting-user-permissions.md)
-   [Recuperando e definindo propriedades do sensor](setting-and-retrieving-sensor-properties.md)
-   [Verificando os campos de dados de sensor com suporte](checking-for-supported-sensor-data-fields.md)
-   [Usando eventos de API do sensor](using-sensor-api-events.md)
-   [Recuperando valores de dados de sensor](retrieving-sensor-data-fields.md)
-   [Recuperando tipos de vetor](retrieving-vector-types.md)
-   [Usando sensores lógicos](using-logical-sensors.md)
-   [Criando Light-Aware interfaces de usuário](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API do sensor](about-the-sensor-api.md)
</dt> </dl>

 

 



