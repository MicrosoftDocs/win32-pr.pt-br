---
title: Propriedade IMsRdpClientAdvancedSettings5 AudioRedirectionMode
description: Define e recupera o modo de redirecionamento de áudio e diferentes opções de redirecionamento de áudio.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota
- A propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota interface , IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade AudioRedirectionMode
- A propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade AudioRedirectionMode
- A propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade AudioRedirectionMode
- A propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4216b4babf74e5e5f15994c0d8387e0d5087c4f69e4d0245b59cb5765dfe88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352508"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a>Propriedade IMsRdpClientAdvancedSettings5::AudioRedirectionMode

Define e recupera o modo de redirecionamento de áudio e diferentes opções de redirecionamento de áudio.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a>Valor da propriedade

Define valores diferentes para o modo de redirecionamento de áudio. Esse parâmetro tem os seguintes valores possíveis.

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

**AUDIO \_ MODE \_ REDIRECT 0** (o redirecionamento de áudio está habilitado e a opção de redirecionamento é "Traga para este computador". Esse é o modo padrão.)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

**AUDIO \_ MODE \_ PLAY ON SERVER \_ \_ 1** (O redirecionamento de áudio está habilitado e a opção é "Sair no computador remoto". A opção "Sair no computador remoto" só tem suporte ao se conectar remotamente a um computador host que está executando Windows Vista. Se a conexão for com um computador host que está executando o Windows Server 2008, a opção "Sair no computador remoto" será alterada para "Não reproduzir".)


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

**AUDIO \_ MODE \_ NONE 2** (o redirecionamento de áudio está habilitado e o modo é "Não reproduzir".)


</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





