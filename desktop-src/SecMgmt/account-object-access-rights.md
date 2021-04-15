---
description: O tipo de direitos de acesso a objeto de conta tem os seguintes tipos de acesso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Direitos de acesso a objeto de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506059"
---
# <a name="account-object-access-rights"></a>Direitos de acesso a objeto de conta

O tipo de direitos de acesso a objeto de conta tem os seguintes tipos de acesso.



| Tipo de acesso                     | Descrição                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exibição de conta \_                   | Esse tipo de acesso é necessário para ler as informações da conta. Isso inclui os [*privilégios*](/windows/desktop/SecGloss/p-gly) atribuídos à conta, cotas de memória atribuídas e todos os tipos de acesso especiais concedidos. |
| \_privilégios de ajuste de conta \_     | Esse tipo de acesso é necessário para atribuir privilégios ou remover privilégios de uma conta.                                                                                                                                                            |
| \_cotas de ajuste de conta \_         | Esse tipo de acesso é necessário para alterar as cotas de sistema atribuídas a uma conta.                                                                                                                                                                      |
| CONTA \_ ajustar \_ acesso ao sistema \_ | Esse tipo de acesso é necessário para atualizar os sinalizadores de acesso do sistema para a conta.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Máscaras de acesso genérico

O objeto de [**conta**](account-object.md) publica os seguintes mapeamentos de tipos de acesso genéricos para tipos de acesso específicos.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipos de acesso padrão

Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE. Todos os tipos de acesso necessários têm suporte. A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é a seguinte.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
