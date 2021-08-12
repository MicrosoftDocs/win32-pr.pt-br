---
title: Propriedade IMsRdpClientNonScriptable3 WarnAboutClipboardRedirection
description: Especifica ou recupera se a caixa de diálogo de aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota
- A propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- A propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- A propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota objeto , MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
- Propriedade WarnAboutClipboardRedirection Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota , propriedade WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f9b0865b8d7e1b374cd0f8f7ebc47a817f8ca79e0156a57f24971456733532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607665"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>Propriedade IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection

Especifica ou recupera se a caixa de diálogo de aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica se a caixa de diálogo de aviso de segurança deve ser exibida para avisar os usuários sobre o redirecionamento da área de transferência.

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

 

 





