---
title: Função MpHandleClose (MpClient.h)
description: Fecha o handle retornado por MpManagerOpen, MpScanStart, MpThreatOpen ou MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Função MpHandleClose herdado Windows ambiente
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0de52af82589b78805506d57df5e0aa779982741a21805b821163ad0d479c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883493"
---
# <a name="mphandleclose-function"></a>Função MpHandleClose

Fecha o handle retornado por [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)ou [**MpUpdateStart**](mpupdatestart.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ Em\]
</dt> <dd>

Tipo: **MPHANDLE**

Manipular para fechar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem-sucedida, o valor de retorno **será S \_ OK.**

Se a função falhar, o valor de retorno será um código **HRESULT com** falha. O chamador pode usar a [**função MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

O seguinte erro específico pode ser retornado pela função :

| Código de retorno             | Descrição                      |
|-------------------------|----------------------------------|
| E \_ WIN \_ INVALID \_ HANDLE | O handle especificado é inválido. |



 

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
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> </dl>

 

 





