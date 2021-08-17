---
description: Sugestões de design para o desenvolvimento de um CRM COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Sugestões de design para o desenvolvimento de um CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128748"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Sugestões de design para o desenvolvimento de um CRM COM+

Veja a seguir as etapas sugeridas para o desenvolvimento de um CRM COM+:

1.  Antes de iniciar o desenvolvimento, defina o tempo limite da transação como zero (usando a ferramenta administrativa serviços de componentes). defina o sinalizador do registro VTRACE1 (consulte [Configurações de registro do COM+ CRM](com--crm-registry-settings.md)) para ver as mensagens de aviso e de erro do crm no rastreamento de depuração.
2.  Determine qual conjunto de interfaces você precisa usar, estruturado (variantes) ou não estruturado. (Consulte [interfaces do CRM do com+](com--crm-interfaces.md).) isso dependerá do idioma que você usa para desenvolver seu CRM, por exemplo, Microsoft Visual C++ ou Microsoft Visual Basic.
3.  Desenvolva primeiro o trabalhador do CRM. Determine as informações necessárias nos registros de log. Defina os tipos de registros de log necessários e seu formato.
4.  um compensador de crm de depuração é fornecido como parte dos exemplos de crm (no SDK do Windows). Isso pode ser usado temporariamente ao depurar o trabalho do CRM no lugar do compensador de CRM real.
5.  Quando o trabalho do CRM estiver funcionando corretamente, desenvolva o compensador de CRM real e substitua o compensador de CRM de depuração pelo compensador de CRM real.
6.  Pode ser desejável inicialmente não testar o caso de recuperação. Nesse caso, exclua o arquivo de log do CRM para o aplicativo do servidor CRM sempre antes de iniciar esse aplicativo do CRM Server.

## <a name="considerations"></a>Considerações

1.  **Write-ahead.** O componente de trabalho do CRM deve fazer write-ahead; ou seja, ele deve gravar um registro de log indicando que vai executar uma ação antes de realmente executar essa ação. Além disso, esse registro de log deve ser forçado para o disco após a gravação e antes da ação ser executada.
2.  **Isolado.** O CRM não impõe o isolamento. O design de CRM deve fornecer isolamento entre vários clientes em transações separadas e também deve considerar o caso antes da recuperação.
3.  **Recuperação em andamento.** O trabalho do CRM deve lidar com o código de erro "recuperação em andamento". Consulte [Solucionando problemas do CRM com+](troubleshooting-the-com--crm.md) para obter mais informações sobre esse código de erro.
4.  **Tratamento de erros.** O trabalhador do CRM deve lidar com o caso em que a transação é anulada antes do esperado. Consulte a seção [tratamento de erros no CRM do com+](error-handling-in-the-com--crm.md).
5.  **Tempo de recuperação.** O compensador de CRM deve ser criado para executar a recuperação rapidamente para que o novo trabalho para esse aplicativo do CRM Server não precise esperar.
6.  **Idempotência.** É possível que um compensador de CRM receba o mesmo registro de log novamente, para desfazer ou refazer uma ação que já foi desfeita ou refeita. Ações que o compensador de CRM pode executar devem ser idempotentes, o que geralmente significa que os códigos de erro retornados dessas ações devem ser ignorados.
7.  **Inicialização da recuperação.** A recuperação de um aplicativo do servidor CRM é executada quando o aplicativo do servidor CRM é iniciado. No entanto, não há nenhuma inicialização automática de um aplicativo do servidor CRM. O desenvolvedor do aplicativo deve considerar como a inicialização e a recuperação devem ser iniciadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



