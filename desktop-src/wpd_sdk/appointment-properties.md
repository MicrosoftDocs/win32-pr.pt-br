---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de compromisso.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Propriedades do compromisso (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796098"
---
# <a name="appointment-properties"></a>Propriedades do compromisso

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de compromisso.



| Propriedade                                   | VarType        | Descrição                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **\_ \_ participantes aceitos do compromisso WPD \_**  | **LPWStr do VT \_** | Lista delimitada por ponto e vírgula de participantes que aceitaram o compromisso.             |
| **\_ \_ participantes recusados do compromisso WPD \_**  | **LPWStr do VT \_** | Lista delimitada por ponto e vírgula de participantes que recusaram o compromisso.             |
| **\_local do compromisso WPD \_**             | LPWStr do VT \_     | Um local amigável para leitores do compromisso, por exemplo, "prédio 5, sala 7".    |
| **\_ \_ participantes opcionais de compromisso WPD \_**  | **LPWStr do VT \_** | Lista delimitada por ponto e vírgula de participantes opcionais para o compromisso.                  |
| **\_ \_ participantes necessários para o compromisso WPD \_**  | **LPWStr do VT \_** | Lista delimitada por ponto-e-vírgula dos participantes necessários para o compromisso.                  |
| **\_recursos de compromisso WPD \_**            | **LPWStr do VT \_** | Lista delimitada por ponto e vírgula dos recursos necessários para o compromisso.                  |
| **\_ \_ participantes provisórios do compromisso WPD \_** | **LPWStr do VT \_** | Lista delimitada por ponto e vírgula de participantes que aceitou provisoriamente o compromisso. |
| **\_tipo de compromisso WPD \_**                 | **LPWStr do VT \_** | O tipo de compromisso, por exemplo, "pessoal", "negócios" e assim por diante.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




