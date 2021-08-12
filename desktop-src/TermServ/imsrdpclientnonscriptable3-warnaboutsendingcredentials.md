---
title: Propriedade IMsRdpClientNonScriptable3 WarnAboutSendingCredentials
description: Especifica ou recupera se a caixa de diálogo de aviso de segurança deve incluir um aviso sobre como enviar credenciais para o servidor remoto antes de iniciar uma sessão.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota
- A propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota , propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota , propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota , propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota objeto , MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota propriedade , WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota propriedade , WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota propriedade , WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota propriedade WarnAboutSendingCredentials
- Propriedade WarnAboutSendingCredentials Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota propriedade , WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48924b435e09b002992e6380ef130a1e11ca4961dbb0d3514b8c551f21f1b648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607675"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>Propriedade IMsRdpClientNonScriptable3::WarnAboutSendingCredentials

Especifica ou recupera se a caixa de diálogo de aviso de segurança deve incluir um aviso sobre como enviar credenciais para o servidor remoto antes de iniciar uma sessão.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica se a caixa de diálogo de aviso de segurança deve incluir um aviso sobre como enviar credenciais para o servidor remoto antes de iniciar uma sessão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





