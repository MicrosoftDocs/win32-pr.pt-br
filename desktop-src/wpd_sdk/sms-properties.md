---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades do SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propriedades do SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815519"
---
# <a name="sms-properties"></a>Propriedades do SMS

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades do SMS.



| Propriedade                   | VarType        | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_codificação de SMS WPD \_**     | **LPWStr do VT \_** | Um valor que especifica como o driver codificará a mensagem de texto enviada pelo cliente. Esta é uma propriedade somente leitura; o cliente não pode especificar qual tipo de codificação um dispositivo usa para enviar mensagens. Esses valores duplicam os valores enumerados dos [**\_ tipos de \_ codificação \_ do SMS WPD**](wpd-sms-encoding-types.md) . |
| **\_ \_ carga máxima de SMS WPD \_** | **\_UI4 VT**    | O número máximo de bytes que podem estar contidos em uma mensagem.                                                                                                                                                                                                                                             |
| **\_provedor de SMS WPD \_**     | **LPWStr do VT \_** | O nome do provedor de serviços.                                                                                                                                                                                                                                                                                |
| **\_tempo limite de SMS WPD \_**      | **\_UI4 VT**    | O número de milissegundos até que um tempo limite seja retornado.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




