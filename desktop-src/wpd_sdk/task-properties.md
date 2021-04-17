---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de tarefa.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propriedades da tarefa (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762416"
---
# <a name="task-properties"></a>Propriedades da tarefa

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de tarefa.



| Propriedade                         | VarType        | Descrição                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **\_proprietário da tarefa WPD \_**             | **LPWStr do VT \_** | O proprietário da tarefa.                                                                      |
| **\_porcentagem de tarefa WPD \_ \_ concluída** | **\_UI4 VT**    | Um número entre 0 e 100 que especifica como concluir a tarefa.                         |
| **\_data do \_ lembrete da tarefa WPD \_**    | **Data de VT \_**   | Um valor que especifica quando um lembrete deve ser enviado para executar a tarefa, se não for concluído. |
| **\_status da tarefa WPD \_**            | **LPWStr do VT \_** | Uma descrição da cadeia de caracteres do status da tarefa, por exemplo, "em andamento".                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




