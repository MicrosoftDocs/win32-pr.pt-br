---
title: Função DDCCISetVCPFeature
description: Define o valor de um código Painel de Controle VCP (Virtual Painel de Controle) para um monitor.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configuração do monitor da função DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecbfb6172ffd61dd7882895c0db15baddf28986493b202e2fd873135cee41d76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806144"
---
# <a name="ddccisetvcpfeature-function"></a>Função DDCCISetVCPFeature

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Define o valor de um código Painel de Controle VCP (Virtual Painel de Controle) para um monitor.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMonitor* \[ Em\]
</dt> <dd>

Um alça para um monitor físico.

</dd> <dt>

*dwVCPCode* \[ Em\]
</dt> <dd>

O código VCP a ser definido.

</dd> <dt>

*dwNewValue* \[ Em\]
</dt> <dd>

O valor do código VCP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará STATUS \_ SUCCESS.** Caso contrário, retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Os aplicativos [**devem chamar SetVCPFeature em**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) vez de chamar essa função.

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

 

