---
title: Propriedade IMsRdpClientSecuredSettings AudioRedirectionMode
description: Especifica as configurações de redirecionamento de áudio, que especificam se deseja redirecionar sons ou reproduzir sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AudioRedirectionMode
- Propriedade AudioRedirectionMode Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499843"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>Propriedade IMsRdpClientSecuredSettings:: AudioRedirectionMode

Especifica as configurações de redirecionamento de áudio, que especificam se deseja redirecionar sons ou reproduzir sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Valor da propriedade

As novas configurações. Esse parâmetro pode usar um dos valores a seguir.

<dt>

0
</dt> <dd>

Redirecionar sons para o cliente. Este é o valor padrão.

</dd> <dt>

1
</dt> <dd>

Reproduzir sons no computador remoto.

</dd> <dt>

2
</dt> <dd>

Desabilitar o redirecionamento de som; não reproduza sons no servidor.

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Essas propriedades não podem ser definidas quando o controle está conectado.

Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings é definido como 605befcf-39c1-45CC-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





