---
description: Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de email.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propriedades de email (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c67a341bcc7fcac041f02cc183c02e024e60b121150aba0ce62da2f973ccbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843228"
---
# <a name="email-properties"></a>Propriedades de email

Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de email.



| Propriedade                         | VarType        | Descrição                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **LINHA \_ BCC DE EMAIL WPD \_ \_**        | **VT \_ LPWSTR** | Os destinatários BCC da mensagem de email. Os destinatários do BCC recebem uma cópia do email, mas seus nomes não são exibidos como destinatários.   |
| **WPD \_ EMAIL \_ CC \_ LINE**         | **VT \_ LPWSTR** | Os destinatários cc da mensagem de email. Os destinatários cc recebem uma cópia da mensagem de email e seus nomes são exibidos como destinatários. |
| **O EMAIL WPD \_ \_ TEM \_ ANEXOS** | **BOOL da VT \_**   | Um valor booliana que especifica se essa mensagem de email tem anexos.                                                               |
| **O EMAIL WPD \_ \_ FOI \_ \_ LIDO**  | **BOOL da VT \_**   | Um valor booliana que especifica se essa mensagem de email foi lida.                                                                 |
| **HORA DE \_ ENVIO DE EMAIL \_ WPD \_**   | **DATA \_ DA VT**   | Um valor que especifica quando a mensagem de email foi recebida.                                                                              |
| **ENDEREÇO DO \_ REMETENTE DO EMAIL \_ \_ WPD**  | **VT \_ LPWSTR** | O endereço de email do remetente.                                                                                                         |
| **WPD \_ EMAIL \_ TO \_ LINE**         | **VT \_ LPWSTR** | Os principais destinatários da mensagem de email.                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




