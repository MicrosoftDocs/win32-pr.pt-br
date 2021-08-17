---
description: Objeto de serviço
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445576"
---
# <a name="service-object"></a>Objeto de serviço

O objeto de serviço deve dar suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                                      | Obrigatório ou opcional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obrigatórios. .                                                                           |
| [\_ \_ ID pai do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obrigatórios.                                                                             |
| [\_nome do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obrigatórios.                                                                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obrigatórios.                                                                             |
| [objeto WPD- \_ \_ oculto](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Necessário se o objeto de serviço não deve ser mostrado ao usuário.                       |
| [IsSystem de \_ objetos WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Necessário se o objeto for um objeto do sistema (por exemplo, representa um arquivo do sistema). |
| [\_categoria de \_ objeto \_ funcional WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obrigatórios. Isso representa o tipo de serviço do dispositivo, como contatos de serviço.          |
| [\_versão do serviço WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obrigatórios.                                                                             |
| [\_tipo de armazenamento WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Necessário se o serviço for usado para armazenar objetos.                                     |
| [\_capacidade de armazenamento WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Necessário se o serviço for usado para armazenar objetos.                                     |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="typical-formats"></a>Formatos típicos

A lista a seguir identifica os formatos típicos usados pelo objeto de serviço. No entanto, esse objeto não está limitado a esses formatos.

-   \_formato de objeto WPD \_ \_ não especificado

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 
