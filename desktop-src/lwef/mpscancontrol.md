---
title: Função MpScanControl (MpClient. h)
description: Permite o controle de uma verificação que foi iniciada de forma assíncrona via MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Recursos do ambiente Windows herdado da função MpScanControl
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
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455073"
---
# <a name="mpscancontrol-function"></a>Função MpScanControl

Permite o controle de uma verificação que foi iniciada de forma assíncrona via [**MpScanStart**](mpscanstart.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hScanHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para uma operação de verificação assíncrona. Esse identificador é retornado pela função [**MpScanStart**](mpscanstart.md) . Esse parâmetro também pode ser definido como o identificador de interface do Malware Protection Manager retornado pela função [**MpManagerOpen**](mpmanageropen.md) para controlar uma verificação iniciada pelo sistema; nesse caso, o chamador deve ter privilégio administrativo.

</dd> <dt>

*ScanControl* \[ no\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica uma opção de controle de verificação. Esse parâmetro deve ser uma das seguintes opções de controle:



| Valor                                                                                                                                                                  | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_anular MPCONTROL**</dt> </dl>    | Anule a operação de verificação.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**Pausar MPCONTROL \_**</dt> </dl>    | Pause a operação de verificação.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**retomar MPCONTROL \_**</dt> </dl> | Retome a operação de verificação em pausa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





