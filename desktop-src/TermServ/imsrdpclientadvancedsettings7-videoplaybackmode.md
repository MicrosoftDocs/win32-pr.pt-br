---
title: Propriedade IMsRdpClientAdvancedSettings7 VideoPlaybackMode
description: Especifica ou recupera um valor que indica o modo de reprodução de vídeo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade VideoPlaybackMode
- Propriedade VideoPlaybackMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade VideoPlaybackMode
- Propriedade VideoPlaybackMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369930"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>Propriedade IMsRdpClientAdvancedSettings7:: VideoPlaybackMode

Especifica ou recupera um valor que indica o modo de reprodução de vídeo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Valor da propriedade

Um valor que especifica o modo de reprodução de vídeo.

Os valores possíveis são:

<dt>

1
</dt> <dd>

O modo de reprodução de vídeo padrão. Quando o modo de reprodução de vídeo é definido com esse valor, o redirecionamento de vídeo é controlado pela propriedade [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) . Quando a propriedade **AudioRedirectionMode** é definida como **\_ \_ redirecionamento do modo de áudio**, o vídeo é decodificado e renderizado no cliente.

</dd> <dt>

0
</dt> <dd>

O redirecionamento de reprodução de vídeo está desabilitado, mesmo quando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) está definido como **\_ \_ redirecionamento do modo de áudio**. Nesse modo, o vídeo é decodificado e renderizado no servidor de Host da Sessão RD.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





