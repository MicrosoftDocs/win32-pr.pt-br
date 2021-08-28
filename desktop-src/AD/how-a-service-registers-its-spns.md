---
title: Como um serviço registra seus SPNs
description: Antes que um cliente possa usar um SPN para autenticar uma instância de um serviço, o SPN deve ser registrado na conta de usuário ou computador que a instância de serviço usará para fazer logon.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Como um serviço registra seu SPNs AD
- nome da entidade de serviço AD , como um serviço registra seus SPNs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93609ba6205c8075c81204ba5a614a9573d8da5a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881404"
---
# <a name="how-a-service-registers-its-spns"></a>Como um serviço registra seus SPNs

Antes que um cliente possa usar um SPN para autenticar uma instância de um serviço, o SPN deve ser registrado na conta de usuário ou computador que a instância de serviço usará para fazer logon. Normalmente, o registro de SPN é feito por um programa de instalação de serviço em execução com privilégios de administrador de domínio.

O instalador de serviço que instala uma instância de serviço em um computador host normalmente executa o procedimento a seguir.

**Para registrar SPNs para uma instância de serviço**

1.  Chame a [**função DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para criar um ou mais SPNs exclusivos para a instância de serviço. Para obter mais informações, consulte [Formatos de nome para SPNs exclusivos.](name-formats-for-unique-spns.md)
2.  Chame a [**função DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar os nomes na conta de logon do serviço.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registra SPNs como uma propriedade de um objeto de conta de usuário ou computador no diretório. **objetos** de **usuário** e computador têm um atributo **servicePrincipalName,** que é um atributo de vários valores para armazenar todos os SPNs associados a uma conta de usuário ou computador. Se o serviço for executado em uma conta de usuário, os SPNs serão armazenados no **atributo servicePrincipalName** dessa conta. Se o serviço for executado na conta LocalSystem, os SPNs serão armazenados no atributo **servicePrincipalName** da conta do computador host do serviço. O **chamador DsWriteAccountSpn** deve especificar o nome diferenciado do objeto de conta no qual os SPNs são armazenados.

Para garantir que os SPNs registrados sejam seguros, o **atributo servicePrincipalName** não pode ser gravado diretamente; só pode ser gravado chamando [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna). O chamador deve ter acesso de gravação ao **atributo servicePrincipalName** da conta de destino. Normalmente, o acesso de gravação é concedido por padrão apenas aos administradores de domínio. No entanto, há um caso especial em que o sistema permite que um serviço em execução na conta LocalSystem registre seus próprios SPNs na conta de computador do host do serviço. Nesse caso, o SPN que está sendo gravado deve ter o formato " host " e " host " deve ser o nome <service class> / &lt; DNS do &gt; computador &lt; &gt; local.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) também pode remover SPNs de uma conta. Um parâmetro de operação indica se os SPNs devem ser adicionados à conta, removidos da conta ou usados para substituir completamente todos os SPNs atuais da conta. Quando uma instância de serviço é desinstalada, remova os SPNs registrados para essa instância.

Para obter mais informações e um exemplo de código que registra ou registra os SPNs de um serviço, consulte Registrando os [SPNs para um serviço](registering-the-spns-for-a-service.md).

Os serviços baseados em host que usam o formato SPN simples " host ", têm a opção de usar a função <service class> / &lt; &gt; [**DsServerRegisterSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) que cria e registra SPNs para uma instância de serviço. **DsServerRegisterSpn** é uma função auxiliar que chama [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) e [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).

Para obter mais informações, consulte [Contas de logon de serviço](service-logon-accounts.md).

 

 




