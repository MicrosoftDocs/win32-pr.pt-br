---
description: Libera os identificadores Plug and Play (PnP) recuperados pelos métodos IPortableDeviceManager::GetDevices ou IPortableDeviceServiceManager::GetDeviceServices.
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Função FreePortableDevicePnPIDs (PortableDevice.h)
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
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590301"
---
# <a name="freeportabledevicepnpids-function"></a>Função FreePortableDevicePnPIDs

A função auxiliar **FreePortableDevicePnPIDs** libera os identificadores Plug and Play (PnP) recuperados pelos métodos [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ou [**IPortableDeviceServiceManager::GetDeviceServices.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)

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

A matriz de Plug and Play (PnP) a ser liberada.

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

O número de identificadores na matriz especificada pelo *parâmetro pPnPIDs.*

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O aplicativo é responsável por liberar a matriz de ponteiros que ele aloca.

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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho \| UWP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Cabeçalho<br/>                   | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




