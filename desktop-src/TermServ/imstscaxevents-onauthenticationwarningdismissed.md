---
title: Método IMsTscAxEvents OnAuthenticationWarningDismissed
description: Chamado depois que um controle ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAuthenticationWarningDismissed
- Método OnAuthenticationWarningDismissed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369577"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>Método IMsTscAxEvents:: OnAuthenticationWarningDismissed

Chamado depois que um controle ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).

## <a name="syntax"></a>Sintaxe


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se necessário, a propriedade [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) da interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) pode ser usada para reverter qualquer pai que tenha sido feito no método [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2008 com SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





