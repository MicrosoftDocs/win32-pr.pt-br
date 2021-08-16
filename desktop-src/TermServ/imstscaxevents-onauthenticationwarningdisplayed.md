---
title: Método IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Chamado antes de um controle ActiveX exibição de uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro de certificado).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Método OnAuthenticationWarningDisplayed Serviços de Área de Trabalho Remota
- Método OnAuthenticationWarningDisplayed Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota , método OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854004"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>Método IMsTscAxEvents::OnAuthenticationWarningDisplayed

Chamado antes de um controle ActiveX exibição de uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro de certificado).

## <a name="syntax"></a>Sintaxe


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se necessário, a propriedade [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) da interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) pode ser usada para garantir que a caixa de diálogo de autenticação modal a ser exibida seja pai por uma janela especificada (isso pode ser necessário para impedir que os usuários usem outras caixas de diálogo enquanto a caixa de diálogo de autenticação é exibida). Por padrão, o pai é a ActiveX de controle.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

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

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





