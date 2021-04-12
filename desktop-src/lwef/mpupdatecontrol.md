---
title: Função MpUpdateControl (MpClient. h)
description: Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Recursos do ambiente Windows herdado da função MpUpdateControl
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455459"
---
# <a name="mpupdatecontrol-function"></a>Função MpUpdateControl

Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via [**MpUpdateStart**](mpupdatestart.md). Chamar essa função requer privilégio de administrador, pois permite o cancelamento de uma atualização de assinatura em todo o sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hUpdateHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para uma operação de atualização de assinatura assíncrona. Esse identificador é retornado pela função [**MpScanStart**](mpscanstart.md) .

</dd> <dt>

*UpdateControl* \[ no\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica a opção de controle de atualização de assinatura. Ele deve ser o seguinte valor:



| Valor                                                                                                                                                               | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_anular MPCONTROL**</dt> </dl> | Anule a operação de atualização de assinatura.<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





