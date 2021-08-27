---
title: Função MpScanControl (MpClient.h)
description: Permite o controle de uma verificação iniciada de forma assíncrona por meio de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Recursos de ambiente herdados Windows função MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893fe1d01f9004c9dc2933a5bbb23c4b13fb8933a6121c41810c6e447e5eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114546"
---
# <a name="mpscancontrol-function"></a>Função MpScanControl

Permite o controle de uma verificação iniciada de forma assíncrona por meio [**de MpScanStart.**](mpscanstart.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hScanHandle* \[ Em\]
</dt> <dd>

Tipo: **MPHANDLE**

Lidar com uma operação de verificação assíncrona. Esse handle é retornado pela [**função MpScanStart.**](mpscanstart.md) Esse parâmetro também pode ser definido como o identificador de interface do gerenciador de proteção contra malware retornado pela função [**MpManagerOpen**](mpmanageropen.md) para controlar uma verificação iniciada pelo sistema, caso em que o chamador deve ter privilégio administrativo.

</dd> <dt>

*ScanControl* \[ Em\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica uma opção de controle de verificação. Esse parâmetro deve ser uma das seguintes opções de controle:



| Valor                                                                                                                                                                  | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl>    | Anular a operação de verificação.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL \_ PAUSE**</dt> </dl>    | Pause a operação de verificação.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**MPCONTROL \_ RESUME**</dt> </dl> | Retome a operação de verificação em pausa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem-sucedida, o valor de retorno **será S \_ OK.**

Se a função falhar, o valor de retorno será um código **HRESULT com** falha. O chamador pode usar a [**função MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





