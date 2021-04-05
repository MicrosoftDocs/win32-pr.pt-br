---
title: Mensagem de DRV_OPEN (mmsystem. h)
description: Direciona o driver para abrir uma nova instância.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- Multimídia do Windows de mensagem DRV_OPEN
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086403"
---
# <a name="drv_open-message"></a>\_Abrir mensagem drv

Direciona o driver para abrir uma nova instância.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador do driver instalável.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador da instância de driver instalável.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Endereço de uma cadeia de caracteres largos, terminada em nulo, que especifica as informações de configuração usadas para abrir a instância. Se nenhuma informação de configuração estiver disponível, essa cadeia de caracteres estará vazia ou o parâmetro será **nulo**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

dados específicos do driver de 32 bits.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero, se for bem-sucedido ou zero.

## <a name="remarks"></a>Comentários

Se o driver retornar um valor diferente de zero, o sistema usará esse valor como o identificador de driver (o parâmetro *dwDriverId* ) nas mensagens que ele enviará subsequentemente para a instância do driver. O driver pode retornar qualquer tipo de valor como o identificador. Por exemplo, alguns drivers retornam endereços de memória que apontam para informações específicas da instância. O uso desse método de especificação de identificadores para uma instância de driver fornece aos drivers acesso imediato às informações enquanto eles estão processando mensagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





