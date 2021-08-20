---
title: Função GetNumberOfPhysicalMonitors
description: Obtém o número de monitores filos associados a um dispositivo de exibição.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configuração do Monitor da função GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673ef12d1e02d87e068784408824bb78dbbbad5dfd5c907ece58c3eb7673e957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534926"
---
# <a name="getnumberofphysicalmonitors-function"></a>Função GetNumberOfPhysicalMonitors

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Obtém o número de monitores filos associados a um dispositivo de exibição.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pstrDeviceName* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ STRING UNICODE**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de exibição, conforme retornado pela [**função GetMonitorInfo.**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*pdwNumberOfPhysicalMonitors* \[ out\]
</dt> <dd>

Recebe o número de monitores físicos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará STATUS \_ SUCCESS.** Caso contrário, retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:

-   [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

Essa função não tem nenhuma biblioteca de importação associada. Para chamar essa função, você deve usar as [**funções LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Monitorar funções de configuração](monitor-configuration-functions.md)
</dt> </dl>

 

