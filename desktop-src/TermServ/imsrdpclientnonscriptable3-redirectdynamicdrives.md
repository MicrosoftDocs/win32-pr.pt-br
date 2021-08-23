---
title: Propriedade RedirectDynamicDrives de IMsRdpClientNonScriptable3
description: Especifica ou recupera se as unidades pnP (Plug and Play) anexadas dinamicamente que são enumeradas em uma sessão estão disponíveis para redirecionamento.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota
- A propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- A propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- A propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota objeto , MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- A propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
- Propriedade RedirectDynamicDrives Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota propriedade RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199f8fcf8e114cfb8febd05631e49de97aab01a69ca9397bc7d15539ad819d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001096"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>Propriedade IMsRdpClientNonScriptable3::RedirectDynamicDrives

Especifica ou recupera se as unidades pnP (Plug and Play) anexadas dinamicamente que são enumeradas em uma sessão estão disponíveis para redirecionamento.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica se as unidades PnP anexadas dinamicamente que são enumeradas em uma sessão estão disponíveis para redirecionamento.

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

 

 





