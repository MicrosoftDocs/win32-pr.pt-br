---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Práticas recomendadas para minimizar serviços sem resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837177"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Práticas recomendadas para minimizar serviços sem resposta

## <a name="affected-platform"></a>Plataforma afetada

 **Clientes** – Windows Vista \| Windows 7  

## <a name="description"></a>Descrição

Os serviços sem resposta podem resultar em tempos limite, sessões encerradas e até mesmo perda de dados. O emprego das práticas recomendadas pode reduzir muito a ocorrência de serviços sem resposta.

## <a name="best-practices"></a>Práticas Recomendadas

Verifique se seus aplicativos e todos os seus serviços e drivers dependentes respondem às notificações de energia e desligamento do sistema.

-   Todos os aplicativos devem responder de forma imediata e apropriada para desligar mensagens como o WM \_ QUERYENDSESSION e \_ o WM EndSession que indicam que um desligamento está em andamento.
-   Todos os serviços devem responder imediatamente às notificações de desligamento do SCM. Se eles não conseguirem fazer isso, o computador os tratará como sem resposta e iniciará um tempo limite de 20 segundos e os interromperá, abrindo a possibilidade de perda de dados. Isso também adiciona 20 segundos ao tempo de desligamento de um computador desligado.
-   Todos os serviços que têm dependências de driver de dispositivo de kernel devem responder imediatamente e adequadamente para a \_ \_ notificação de desligamento do IRP MJ em suas rotinas de DispatchShutdown.

## <a name="links-to-other-resources"></a>Links para outros recursos

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



