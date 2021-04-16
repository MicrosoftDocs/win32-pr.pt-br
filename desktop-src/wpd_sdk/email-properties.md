---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de email.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propriedades de email (PortableDevice. h)
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
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759330"
---
# <a name="email-properties"></a>Propriedades de email

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de email.



| Propriedade                         | VarType        | Descrição                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ linha Cco de email WPD \_**        | **LPWStr do VT \_** | Os destinatários Cco da mensagem de email. Os destinatários Cco recebem uma cópia do email, mas seus nomes não são exibidos como destinatários.   |
| **\_ \_ linha CC de email WPD \_**         | **LPWStr do VT \_** | Os destinatários CC da mensagem de email. Os destinatários de CC recebem uma cópia da mensagem de email e seus nomes são exibidos como destinatários. |
| **o \_ email WPD \_ tem \_ anexos** | **BOOL do VT \_**   | Um valor booliano que especifica se esta mensagem de email tem anexos.                                                               |
| **o \_ email WPD foi \_ \_ \_ lido**  | **BOOL do VT \_**   | Um valor booliano que especifica se esta mensagem de email foi lida.                                                                 |
| **\_tempo de \_ recebimento de email WPD \_**   | **Data de VT \_**   | Um valor que especifica quando a mensagem de email foi recebida.                                                                              |
| **\_endereço de \_ remetente de email WPD \_**  | **LPWStr do VT \_** | O endereço de email do remetente.                                                                                                         |
| **\_email WPD \_ para \_ linha**         | **LPWStr do VT \_** | Os principais destinatários da mensagem de email.                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




