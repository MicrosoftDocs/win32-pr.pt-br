---
title: Função MpHandleClose (MpClient. h)
description: Fecha o identificador retornado por MpManagerOpen, MpScanStart, MpThreatOpen ou MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Recursos do ambiente Windows herdado da função MpHandleClose
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
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499700"
---
# <a name="mphandleclose-function"></a>Função MpHandleClose

Fecha o identificador retornado por [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)ou [**MpUpdateStart**](mpupdatestart.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para fechar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

O seguinte erro específico pode ser retornado pela função:

| Código de retorno             | Descrição                      |
|-------------------------|----------------------------------|
| E \_ Win \_ \_ identificador inválido | O identificador especificado é inválido. |



 

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
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> </dl>

 

 





