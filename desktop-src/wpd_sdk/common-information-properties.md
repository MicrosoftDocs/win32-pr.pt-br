---
description: Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de informações comuns.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propriedades de informações comuns (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431099"
---
# <a name="common-information-properties"></a>Propriedades de informações comuns

Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de informações comuns.



| Propriedade                                      | VarType        | Descrição                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **NOTAS DE \_ INFORMAÇÕES \_ COMUNS DO \_ WPD**           | **VT \_ LPWSTR** | Para compromissos, tarefas e objetos semelhantes, essa propriedade contém qualquer anotação para o objeto determinado.     |
| **ASSUNTO DE \_ INFORMAÇÕES \_ COMUNS DO \_ WPD**         | **VT \_ LPWSTR** | Um valor que especifica o campo de assunto desse objeto.                                                 |
| **TEXTO DO \_ CORPO DE INFORMAÇÕES COMUNS \_ \_ WPD \_**      | **VT \_ LPWSTR** | Essa propriedade contém o texto do corpo de um objeto, em formato HTML ou texto não criptografado.                          |
| **PRIORIDADE DE \_ INFORMAÇÕES \_ COMUNS WPD \_**        | **VT \_ UI4**    | Um valor que especifica a prioridade desse objeto. 0 indica a prioridade mais alta.                    |
| **WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME** | **DATA \_ DA VT**   | Um valor que especifica a data/hora em que um compromisso, tarefa ou objeto semelhante está agendado para iniciar. |
| **WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME**   | **DATA \_ DA VT**   | Um valor que especifica a data/hora em que um compromisso, tarefa ou objeto semelhante está agendado para terminar.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




