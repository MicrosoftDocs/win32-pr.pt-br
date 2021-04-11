---
title: Propriedade IMsRdpClientNonScriptable4 WarnAboutPrinterRedirection
description: Controla se a caixa de diálogo redirecionamento exibe uma mensagem sobre o redirecionamento de impressora antes de iniciar uma sessão.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295809"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a>Propriedade IMsRdpClientNonScriptable4:: WarnAboutPrinterRedirection

Controla se a caixa de diálogo redirecionamento exibe uma mensagem sobre o redirecionamento de impressora antes de iniciar uma sessão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor da propriedade

Define se a caixa de diálogo de redirecionamento exibe uma mensagem sobre o redirecionamento de impressora.

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

 

 





