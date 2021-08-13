---
description: Objeto service
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445576"
---
# <a name="service-object"></a>Objeto service

O objeto de serviço deve dar suporte às propriedades a seguir.



| Nome da Propriedade                                                                                                                      | Obrigatório ou Opcional                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | Obrigatórios. .                                                                           |
| [ID PAI \_ \_ DO OBJETO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | Obrigatórios.                                                                             |
| [NOME DO OBJETO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | Obrigatórios.                                                                             |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | Obrigatórios.                                                                             |
| [\_ \_ ISHIDDEN DE OBJETO WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Necessário se o objeto de serviço não deve ser mostrado ao usuário.                       |
| [ISSYSTEM \_ DO OBJETO WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Necessário se o objeto for um objeto do sistema (por exemplo, ele representa um arquivo do sistema). |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | Obrigatórios. Isso representa o tipo de Serviço de Dispositivo, como Contatos DE SERVIÇO.          |
| [VERSÃO DO SERVIÇO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | Obrigatórios.                                                                             |
| [TIPO DE \_ ARMAZENAMENTO \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | Necessário se o serviço for usado para armazenar objetos.                                     |
| [CAPACIDADE DE ARMAZENAMENTO WPD \_ \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | Necessário se o serviço for usado para armazenar objetos.                                     |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="typical-formats"></a>Formatos típicos

A lista a seguir identifica formatos típicos usados pelo objeto Service. No entanto, esse objeto não está limitado a esses formatos.

-   FORMATO DE OBJETO WPD \_ \_ NÃO \_ ESPECIFICADO

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 
