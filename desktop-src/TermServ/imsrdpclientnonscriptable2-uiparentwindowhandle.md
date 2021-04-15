---
title: Propriedade IMsRdpClientNonScriptable2 UIParentWindowHandle
description: Define ou recupera o identificador de janela como a janela pai de qualquer caixa de diálogo exibida pelo controle. Isso permite que qualquer janela exibida pelo controle seja devidamente modal com relação a todas as janelas exibidas pelo aplicativo pai.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade UIParentWindowHandle
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454649"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a>Propriedade IMsRdpClientNonScriptable2:: UIParentWindowHandle

Define ou recupera o identificador de janela como a janela pai de qualquer caixa de diálogo exibida pelo controle. Isso permite que qualquer janela exibida pelo controle seja devidamente modal com relação a todas as janelas exibidas pelo aplicativo pai.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a>Valor da propriedade

O novo identificador de janela.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2008 com SP1<br/>                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 é definido como 17a5e535-4072-4fa4-AF32-c8d0d47345e9<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





