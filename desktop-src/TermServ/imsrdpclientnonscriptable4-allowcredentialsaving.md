---
title: Propriedade IMsRdpClientNonScriptable4 AllowCredentialSaving
description: Especifica se a caixa de diálogo credenciais exibe uma caixa de seleção que permite a economia de credenciais.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota
- A propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota interface , IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota , propriedade AllowCredentialSaving
- A propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota interface , IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota , propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota propriedade , AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota propriedade , AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota propriedade , AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota propriedade , AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cca6f61b8cbcc315eb93e6e9c3ab0f89684e4d29c3fcb8313af0198ee594cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607722"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a>Propriedade IMsRdpClientNonScriptable4::AllowCredentialSaving

Especifica se a caixa de diálogo credenciais exibe uma caixa de seleção que permite a economia de credenciais.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a>Valor da propriedade

Define se a caixa de diálogo credenciais exibe uma caixa de seleção que habilita a economia de credenciais.

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

 

 





