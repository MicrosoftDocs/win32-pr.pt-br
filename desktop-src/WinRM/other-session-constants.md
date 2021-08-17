---
title: Outras constantes de sessão (WSManDisp. h)
description: Especifique a codificação, a criptografia e a porta do nome da entidade de serviço.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd9d2cf44063dfb1a7ec1bfcbb0fe785d1747d34e84ef2c2d8c78598e6e6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743321"
---
# <a name="other-session-constants"></a>Outras constantes de sessão

Constantes, listadas na lista a seguir, na enumeração **\_ \_ WSManSessionFlags** que especificam a codificação, a criptografia e a porta do nome da entidade de serviço.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Envia a solicitação em UTF8 em vez de UTF16.

O método de script associado é [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) e o método C++ é [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Não criptografe as mensagens enviadas pela rede. Essa configuração só será permitida se o [*ouvinte*](windows-remote-management-glossary.md) estiver configurado para que **AllowUnencrypted** seja definido como **true**.

O método de script associado é [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) e o método C++ é [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Especifique a porta do SPN (nome da entidade de serviço) ao se conectar diretamente ao hardware do BMC remoto, também conhecido como uma conexão [*fora de banda*](windows-remote-management-glossary.md) . Como o computador do servidor WinRM e o hardware BMC podem compartilhar o mesmo endereço IP, esse sinalizador indica que o número da porta SPN deve ser usado para determinar se a conexão é para o serviço ou diretamente para o BMC. Para obter mais informações, consulte [formatos de nome para SPNs exclusivos](/windows/desktop/AD/name-formats-for-unique-spns).

O método de script associado é [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) e o método C++ é [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Envia a solicitação em UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de sessão](session-constants.md)
</dt> </dl>

 

