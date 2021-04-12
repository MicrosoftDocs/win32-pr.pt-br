---
title: Propriedade IMsRdpClientNonScriptable4 PromptForCredsOnClient
description: Especifica se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369734"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4: Propriedade romptForCredsOnClient de:P

Especifica se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Valor da propriedade

Define se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





