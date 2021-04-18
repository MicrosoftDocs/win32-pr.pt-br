---
description: Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a função chamada ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitações de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755308"
---
# <a name="service-control-requests"></a>Solicitações de controle de serviço

Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Essa função especifica um valor de controle que é passado para a função [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) do serviço especificado. Esse valor de controle pode ser um código definido pelo usuário ou pode ser um dos códigos padrão que permitem que o programa de chamada Execute as seguintes ações:

-   Parar um serviço (parada de controle de serviço \_ \_ ).
-   Pausar um serviço ( \_ pausa de controle de serviço \_ ).
-   Retomar a execução de um serviço em pausa (continuação do controle de serviço \_ \_ ).
-   Recuperar informações de status atualizadas de um serviço ( \_ interrogação de controle de serviço \_ ).

Cada serviço especifica os valores de controle que serão aceitos e processados. Para determinar quais dos valores de controle padrão são aceitos por um serviço, use a função [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ou especifique o \_ valor de controle INTERROGATE de controle de serviço \_ em uma chamada para a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . O membro **dwControlsAccepted** da estrutura [**de \_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) retornada por essas funções indica se o serviço pode ser interrompido, pausado ou retomado. Todos os serviços aceitam \_ o \_ valor de controle INTERROGATE de controle de serviço.

A função [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) relata o status mais recente de um serviço especificado, mas não obtém um status atualizado do próprio serviço. O uso do \_ valor de controle INTERROGATE de controle de serviço \_ em uma chamada para [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garante que as informações de status retornadas sejam atuais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando um serviço usando SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



