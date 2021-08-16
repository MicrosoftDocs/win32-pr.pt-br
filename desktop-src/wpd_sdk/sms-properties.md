---
description: Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propriedades de SMS (PortableDevice.h)
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
ms.openlocfilehash: 12b68a962fc79dd75d6ff90635be5dbe99f36c3170f06cd7d79af2eb23317e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193577"
---
# <a name="sms-properties"></a>Propriedades de SMS

Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de SMS.



| Propriedade                   | VarType        | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CODIFICAÇÃO DE \_ SMS \_ WPD**     | **VT \_ LPWSTR** | Um valor que especifica como o driver codifica a mensagem de texto enviada pelo cliente. Essa é uma propriedade somente leitura; o cliente não pode especificar qual tipo de codificação um dispositivo usa para enviar mensagens. Esses valores duplicam [**os valores \_ enumerados WPD SMS \_ ENCODING \_ TYPES.**](wpd-sms-encoding-types.md) |
| **PAYLOAD \_ MÁXIMO DE SMS WPD \_ \_** | **VT \_ UI4**    | O número máximo de bytes que podem ser contidos em uma mensagem.                                                                                                                                                                                                                                             |
| **PROVEDOR DE \_ SMS \_ WPD**     | **VT \_ LPWSTR** | O nome do provedor de serviços.                                                                                                                                                                                                                                                                                |
| **WPD \_ SMS \_ TIMEOUT**      | **VT \_ UI4**    | O número de milissegundos até que um tempoout seja retornado.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




