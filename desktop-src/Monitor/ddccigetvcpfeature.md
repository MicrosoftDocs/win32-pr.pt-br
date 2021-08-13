---
title: Função DDCCIGetVCPFeature
description: Obtém o valor atual, o valor máximo e o tipo de código de um vcp (virtual Painel de Controle) para um monitor.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuração do monitor da função DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640994"
---
# <a name="ddccigetvcpfeature-function"></a>Função DDCCIGetVCPFeature

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Obtém o valor atual, o valor máximo e o tipo de código de um vcp (virtual Painel de Controle) para um monitor.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
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

O código VCP a ser consultado.

</dd> <dt>

*pvct* \[ out, opcional\]
</dt> <dd>

Recebe o tipo de código VCP, como um membro da [**enumeração MC \_ VCP \_ CODE \_ TYPE.**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type)

</dd> <dt>

*pdwCurrentValue* \[ out\]
</dt> <dd>

Recebe o valor atual do código VCP.

</dd> <dt>

*pdwMaximumValue* \[ out, opcional\]
</dt> <dd>

Recebe o valor máximo do código VCP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará STATUS \_ SUCCESS.** Caso contrário, retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Os aplicativos [**devem chamar GetVCPFeatureAndVCPFeatureReply em**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) vez de chamar essa função.

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

 

