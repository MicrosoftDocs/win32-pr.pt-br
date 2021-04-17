---
description: Durante a inicialização do sistema, o SCM inicia todos os serviços de início automático e os serviços dos quais eles dependem. Por exemplo, se um serviço de início automático depender de um serviço de início de demanda, o serviço de início de demanda também será iniciado automaticamente.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Iniciando serviços automaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762895"
---
# <a name="automatically-starting-services"></a>Iniciando serviços automaticamente

Durante a inicialização do sistema, o SCM inicia todos os serviços de início automático e os serviços dos quais eles dependem. Por exemplo, se um serviço de início automático depender de um serviço de início de demanda, o serviço de início de demanda também será iniciado automaticamente.

A ordem de carregamento é determinada pelo seguinte:

1.  A ordem dos grupos na lista de grupos de ordenação de carregamento. Essas informações são armazenadas no valor **ServiceGroupOrder** na seguinte chave do registro:

    **HKEY \_ \_ computador local \\ sistema \\ CurrentControlSet \\ Control**

    Para especificar o grupo de ordenação de carga para um serviço, use o parâmetro *lpLoadOrderGroup* da função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .

2.  A ordem dos serviços dentro de um grupo especificado no vetor de ordem de marcas. Essas informações são armazenadas no valor **GroupOrderList** na seguinte chave do registro:

    **HKEY \_ \_ computador local \\ sistema \\ CurrentControlSet \\ Control**

3.  As dependências listadas para cada serviço.

Quando a inicialização for concluída, o sistema executará o programa de verificação de inicialização especificado pelo valor **BootVerificationProgram** da seguinte chave do registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control**.

Por padrão, esse valor não é definido. O sistema simplesmente relata que a inicialização foi bem-sucedida depois que o primeiro usuário fez logon. Você pode fornecer um programa de verificação de inicialização que verifica o sistema em busca de problemas e relata o status de inicialização para o SCM usando a função [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .

Após uma inicialização bem-sucedida, o sistema salva um clone do banco de dados na última configuração válida (LKG). O sistema pode restaurar essa cópia do banco de dados se as alterações feitas no banco de dados ativo causarem a falha da reinicialização do sistema. A seguir está a chave do registro para este banco de dados:

**HKEY \_ local \_ Machine \\ Control do sistema de \\ controle *xxx* \\ serviços**

em que *xxx* é o valor salvo no seguinte valor de registro: **HKEY \_ local \_ Machine \\ System \\ selecione \\ LastKnownGood**.

Se um serviço de início automático com um erro de serviço \_ \_ crítico não for iniciado, o SCM reinicializará o computador usando a configuração LKG. Se a configuração LKG já estiver sendo usada, a inicialização falhará.

Um serviço de início automático pode ser configurado como um serviço de início automático atrasado chamando a função [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) com informações de \_ \_ início automático atrasadas de configuração de serviço \_ \_ \_ . Essa alteração entra em vigor após a próxima inicialização do sistema. Para obter mais informações, [**consulte \_ \_ informações de \_ início \_ automático com atraso no serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



