---
description: 'Libera os identificadores de plug and Play (PnP) que são recuperados pelos métodos IPortableDeviceManager:: Devices ou IPortableDeviceServiceManager:: getdeviceservices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Função FreePortableDevicePnPIDs (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170687"
---
# <a name="freeportabledevicepnpids-function"></a>Função FreePortableDevicePnPIDs

A função auxiliar **FreePortableDevicePnPIDs** libera os identificadores de plug and Play (PnP) que são recuperados pelos métodos [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ou [**IPortableDeviceServiceManager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .

## <a name="syntax"></a>Sintaxe


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPnPIDs* 
</dt> <dd>

A matriz de identificadores de Plug and Play (PnP) a ser liberada.

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

O número de identificadores na matriz especificada pelo parâmetro *pPnPIDs* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O aplicativo é responsável por liberar a matriz de ponteiros que ela aloca.

## <a name="examples"></a>Exemplos


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| parâmetro<br/>                   | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




