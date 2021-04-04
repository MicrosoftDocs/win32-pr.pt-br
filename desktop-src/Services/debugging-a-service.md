---
description: Você pode usar qualquer um dos métodos a seguir para depurar seu serviço.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Depurar um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646974"
---
# <a name="debugging-a-service"></a>Depurar um serviço

Você pode usar qualquer um dos métodos a seguir para depurar seu serviço.

-   Use o depurador para depurar o serviço enquanto ele estiver em execução. Primeiro, obtenha o identificador do processo (PID) do processo de serviço. Depois de obter a PID, anexe ao processo em execução. Para obter informações de sintaxe, consulte a documentação incluída com o depurador.
-   Chame a função [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) para invocar o depurador para depuração Just-in-time.
-   Especifique um depurador a ser usado ao iniciar um programa. Para fazer isso, crie uma chave chamada **Opções de execução de arquivo de imagem** no seguinte local do registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**

    Crie uma subchave com o mesmo nome que o seu serviço (por exemplo, MYSERV.EXE). Para essa subchave, adicione um valor do tipo **reg \_ sz**, chamado **Debugger**. Use o caminho completo para o depurador como o valor da cadeia de caracteres. No miniaplicativo do painel de controle de serviços, selecione seu serviço, clique em **inicialização** e marque **permitir que o serviço interaja com a área de trabalho**. O serviço deve ser um serviço interativo ou, caso contrário, o depurador não poderá ser executado na área de trabalho padrão. Observe que essa técnica não tem mais suporte do Windows Vista porque todos os serviços são executados na sessão que é reservada exclusivamente para serviços e não oferece suporte à exibição de uma interface do usuário.

-   Use o [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) para registrar informações.

Para depurar o código de inicialização de um serviço de início automático, você precisará instalar e executar temporariamente o serviço como um serviço de início de demanda.

Às vezes, pode ser necessário executar um serviço como um aplicativo de console para fins de depuração. Nesse cenário, a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) retornará **erro \_ falha na \_ conexão do \_ controlador \_ de serviço**. Portanto, não se esqueça de estruturar seu código de modo que o código específico do serviço não seja chamado quando esse erro for retornado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depurando um aplicativo de serviço](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Ferramentas de Depuração para Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
