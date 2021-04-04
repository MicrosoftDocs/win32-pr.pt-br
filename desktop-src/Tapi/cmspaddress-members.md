---
description: A lista a seguir contém os membros do endereço CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membros do CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837480"
---
# <a name="cmspaddress-members"></a>Membros do CMSPAddress



| Tipos de membro                    | Nome                    | Descrição                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| IUnknown                        | \*\_pFTM m               | Ponteiro para o Marshaller com thread livre.                                                         |
| PROCESSAMENTO                          | \_htEvent m              | Manipule o evento de Tapi3.dll, que é usado para notificar a TAPI que o MSP deseja enviar dados para ele. |
| entrada de lista \_                     | de \_ eventos m            | Lista de eventos.                                                                                  |
| CMSPCritSection                 | \_EventDataLock m        | O bloqueio que protege os dados relacionados à manipulação de eventos com a TAPI.                             |
| ITTerminalManager               | \*\_pITTerminalManager m | O ponteiro para o objeto do Gerenciador de terminal.                                                      |
| CMSPArray <ITTerminal \*> | \_terminais m            | A lista de terminais estáticos que podem ser usados no endereço.                                    |
| BOOL                            | \_fTerminalsUpToDate m   | Esse sinalizador será **verdadeiro** se a lista de terminais estiver atualizada.                                        |
| CMSPCritSection                 | \_TerminalDataLock m     | O bloqueio que protege os membros de dados relacionados ao terminal.                                        |



 

 

 



