---
title: Propriedade IMsRdpClientSecuredSettings KeyboardHookMode
description: especifica as configurações de redirecionamento de teclado, que especificam como e quando aplicar Windows atalho de teclado (por exemplo, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade KeyboardHookMode
- Propriedade KeyboardHookMode Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657586"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>Propriedade IMsRdpClientSecuredSettings:: KeyboardHookMode

especifica as configurações de redirecionamento de teclado, que especificam como e quando aplicar Windows atalho de teclado (por exemplo, ALT + TAB).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Valor da propriedade

As novas configurações. Esse parâmetro pode usar um dos valores a seguir.

<dt>

0
</dt> <dd>

Aplicar combinações de teclas somente localmente no computador cliente.

</dd> <dt>

1
</dt> <dd>

Aplicar combinações de chaves no servidor remoto.

</dd> <dt>

2
</dt> <dd>

Aplique combinações de teclas ao servidor remoto somente quando o cliente estiver sendo executado no modo de tela inteira. Esse é o valor padrão.

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

 

 





