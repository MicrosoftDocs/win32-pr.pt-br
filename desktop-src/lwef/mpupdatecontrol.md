---
title: Função MpUpdateControl (MpClient.h)
description: Permite o controle de uma operação de atualização de assinatura iniciada de forma assíncrona por meio de MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Funcionalidade mpUpdateControl herdado Windows ambiente
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
ms.openlocfilehash: 69926f26b470ba41226883bdb32fab13c5d776858595c256fe70e7f95e898c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476268"
---
# <a name="mpupdatecontrol-function"></a>Função MpUpdateControl

Permite o controle de uma operação de atualização de assinatura iniciada de forma assíncrona por meio [**de MpUpdateStart**](mpupdatestart.md). Chamar essa função requer privilégio de administrador, pois permite o cancelamento de uma atualização de assinatura em todo o sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hUpdateHandle* \[ Em\]
</dt> <dd>

Tipo: **MPHANDLE**

Lidar com uma operação de atualização de assinatura assíncrona. Esse handle é retornado pela [**função MpScanStart.**](mpscanstart.md)

</dd> <dt>

*UpdateControl* \[ Em\]
</dt> <dd>

Tipo: **MPCONTROL**

Especifica a opção de controle de atualização de assinatura. Ele deve ser o seguinte valor:



| Valor                                                                                                                                                               | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl> | Anular a operação de atualização de assinatura.<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





