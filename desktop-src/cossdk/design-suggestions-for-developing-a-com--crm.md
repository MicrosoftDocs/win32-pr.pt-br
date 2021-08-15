---
description: Sugestões de design para desenvolver um COM+ CRM
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Sugestões de design para desenvolver um COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128748"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Sugestões de design para desenvolver um COM+ CRM

A seguir estão as etapas sugeridas para desenvolver um COM+ CRM:

1.  Antes de iniciar o desenvolvimento, de definido o tempo de vida da transação como zero (usando a ferramenta administrativa dos Serviços de Componentes). De definir o sinalizador de registro VTRACE1 (consulte [Com+ CRM Registry Configurações](com--crm-registry-settings.md)) para ver mensagens de erro e aviso de CRM no rastreamento de depuração.
2.  Determine qual conjunto de interfaces você precisa usar, estruturado (Variantes) ou não estruturado. (Consulte [Interfaces COM+ CRM](com--crm-interfaces.md).) Isso dependerá da linguagem que você usa para desenvolver seu CRM, por exemplo, Microsoft Visual C++ ou Microsoft Visual Basic.
3.  Desenvolva o trabalho do CRM primeiro. Determine as informações necessárias nos registros de log. Defina os tipos de registros de log necessários e seu formato.
4.  Um compensador de CRM de depuração é fornecido como parte dos exemplos de CRM (no SDK do Windows). Isso pode ser usado temporariamente ao depurar o trabalho do CRM no lugar do compensador de CRM real.
5.  Quando o trabalho do CRM estiver funcionando corretamente, desenvolva o compensador de CRM real e substitua o compensador crm de depuração pelo compensador de CRM real.
6.  Pode ser desejável inicialmente não testar o caso de recuperação. Nesse caso, exclua o arquivo de log crm para o aplicativo de servidor CRM sempre antes de iniciar esse aplicativo de servidor CRM.

## <a name="considerations"></a>Considerações

1.  **Escreva com antecedência.** O componente de trabalho crm deve gravar com antecedência; ou seja, ele deve gravar um registro de log indicando que executará uma ação antes de realmente executar essa ação. Além disso, esse registro de log deve ser forçado para o disco após a gravação e antes que a ação seja executada.
2.  **Isolamento.** O CRM não impõe isolamento. O design crm deve fornecer isolamento entre vários clientes em transações separadas e também deve considerar o caso antes da recuperação.
3.  **Recuperação em andamento.** O trabalho do CRM deve lidar com o código de erro "recuperação em andamento". Consulte [Solução de problemas do COM+ CRM](troubleshooting-the-com--crm.md) para obter mais informações sobre esse código de erro.
4.  **Tratamento de erro.** O trabalho crm deve lidar com o caso em que a transação é anulada antes do esperado. Consulte a seção [Tratamento de erros no COM+ CRM.](error-handling-in-the-com--crm.md)
5.  **Tempo de recuperação.** O compensador crm deve ser projetado para executar a recuperação rapidamente para que o novo trabalho para esse aplicativo de servidor CRM não tenha que esperar.
6.  **Idempotência.** É possível que um compensador de CRM possa receber o mesmo registro de log novamente para desfazer ou refazer uma ação que já foi desfeita ou refeita. As ações que o compensador de CRM pode executar devem ser idempotentes, o que geralmente significa que os códigos de erro retornados dessas ações devem ser ignorados.
7.  **Iniciação da recuperação.** A recuperação de um aplicativo de servidor CRM é executada quando esse aplicativo de servidor CRM é iniciado. No entanto, não há inicialização automática de um aplicativo de servidor CRM. O desenvolvedor do aplicativo deve considerar como a inicialização e a recuperação devem ser iniciadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de Resource Manager com+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



