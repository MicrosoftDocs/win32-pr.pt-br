---
description: Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a função ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitações de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4320aad28f8a176fbf4aaa6b51539256a376a01b8edea034341cae7831ca4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967565"
---
# <a name="service-control-requests"></a>Solicitações de controle de serviço

Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a [**função ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Essa função especifica um valor de controle que é passado para a [**função HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) do serviço especificado. Esse valor de controle pode ser um código definido pelo usuário ou pode ser um dos códigos padrão que permitem que o programa de chamada execute as seguintes ações:

-   Parar um serviço (SERVICE \_ CONTROL \_ STOP).
-   Pausar um serviço (PAUSA \_ DE CONTROLE \_ DE SERVIÇO).
-   Retomar a execução de um serviço em pausa (SERVICE \_ CONTROL \_ CONTINUE).
-   Recuperar informações de status atualizadas de um serviço (SERVICE \_ CONTROL \_ QUESTIONADO).

Cada serviço especifica os valores de controle que ele aceitará e processará. Para determinar quais dos valores de controle padrão são aceitos por um serviço, use a função [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ou especifique o valor do controle SERVICE CONTROL DETERMINE em uma chamada para \_ a função \_ [**ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) O **membro dwControlsAccepted** da estrutura [**\_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) do SERVIÇO retornado por essas funções indica se o serviço pode ser interrompido, pausado ou retomado. Todos os serviços aceitam o valor do controle \_ \_ DE CONTROLE DE SERVIÇO, TAMBÉM.

A [**função QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) relata o status mais recente de um serviço especificado, mas não tem um status atualizado do próprio serviço. Usar o valor do controle SERVICE CONTROL QUESTION EM uma chamada para \_ \_ [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garante que as informações de status retornadas são atuais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando um serviço usando SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



