---
description: Solução de problemas
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810539"
---
# <a name="troubleshooting"></a>Solução de problemas

Se você estiver tendo problemas para diagnosticar os erros do aplicativo, consulte as seguintes dicas de solução de problemas:

-   Verifique se o Coordenador de Transações Distribuídas (DTC) está em execução em todos os servidores.
-   Verifique a comunicação de rede testando primeiro em um computador local para verificar se o aplicativo funciona. Se você estiver executando o TCP/IP em sua rede, poderá usar o utilitário ping.exe para verificar se os computadores estão na rede.
-   Verifique se o SQL e o DTC estão localizados no mesmo computador ou se o programa de configuração do cliente DTC especifica que o DTC está em outro computador. Caso contrário, o SQLConnect retornará um erro internamente quando chamado de um componente transacional.
-   Defina o tempo limite da transação para um número mais alto que o padrão de 60 segundos. Depois que o tempo limite da transação tiver decorrido, o COM+ anulará a transação. Todas as chamadas subsequentes para o componente retornam imediatamente com o contexto \_ E \_ anulado.
-   Certifique-se de que os drivers ODBC sejam thread-safe e não tenham afinidade de thread.
-   Se você tiver dificuldade em fazer com que um aplicativo funcione em vários servidores, reinicialize o cliente e verifique se o controlador de domínio está configurado corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Localizando a origem de um erro](finding-the-source-of-an-error.md)
</dt> <dt>

[Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretando códigos de erro](interpreting-error-codes.md)
</dt> <dt>

[Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



