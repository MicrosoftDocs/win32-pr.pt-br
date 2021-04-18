---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de informações comuns.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propriedades de informações comuns (PortableDevice. h)
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
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787642"
---
# <a name="common-information-properties"></a>Propriedades de informações comuns

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de informações comuns.



| Propriedade                                      | VarType        | Descrição                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **\_observações de \_ informações \_ comuns do WPD**           | **LPWStr do VT \_** | Para compromissos, tarefas e objetos semelhantes, essa propriedade contém todas as anotações para o objeto fornecido.     |
| **\_assunto de \_ informações \_ comuns do WPD**         | **LPWStr do VT \_** | Um valor que especifica o campo de assunto deste objeto.                                                 |
| **\_texto de \_ corpo de informações comuns \_ WPD \_**      | **LPWStr do VT \_** | Essa propriedade contém o texto do corpo de um objeto, em formato HTML ou de texto não criptografado.                          |
| **\_prioridade de \_ informações \_ comuns WPD**        | **\_UI4 VT**    | Um valor que especifica a prioridade deste objeto. 0 indica a prioridade mais alta.                    |
| **\_DateTime de \_ início de informações comuns \_ WPD \_** | **Data de VT \_**   | Um valor que especifica a data/hora em que um compromisso, uma tarefa ou um objeto semelhante está agendado para iniciar. |
| **\_data de \_ término de informações comuns \_ WPD \_**   | **Data de VT \_**   | Um valor que especifica a data/hora em que um compromisso, uma tarefa ou um objeto semelhante está agendado para terminar.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




