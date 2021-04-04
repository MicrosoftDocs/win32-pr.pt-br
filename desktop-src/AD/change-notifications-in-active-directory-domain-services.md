---
title: Notificações de alteração no Active Directory Domain Services
description: Active Directory Domain Services fornecer um mecanismo para que um aplicativo cliente se registre em um controlador de domínio para receber notificações de alteração.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee564727cfbcb2bfdb367f822fdc137bca7c4e37
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007358"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Notificações de alteração no Active Directory Domain Services

Active Directory Domain Services fornecer um mecanismo para que um aplicativo cliente se registre em um controlador de domínio para receber notificações de alteração. Para fazer isso, o cliente especifica o controle de notificação de alteração de LDAP em uma operação de pesquisa LDAP assíncrona. O cliente também especifica os seguintes parâmetros de pesquisa.



| Parâmetro             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escopo<br/>      | Especifique a **\_ \_ base do escopo LDAP** para monitorar apenas o objeto ou **o \_ escopo \_ do LDAP** num para monitorar os filhos imediatos do objeto, não incluindo o próprio objeto. Não especifique a **\_ \_ subárvore do escopo LDAP**. Embora o escopo da subárvore tenha suporte se o objeto base for a raiz de um contexto de nomenclatura, seu uso poderá afetar seriamente o desempenho do servidor, pois ele gera uma mensagem de resultado de pesquisa LDAP toda vez que um objeto no contexto de nomenclatura é modificado. Não é possível especificar a **\_ \_ subárvore de escopo LDAP** para uma subárvore arbitrária.<br/> |
| Filtrar<br/>     | Especifique um filtro de pesquisa de "(objectClass = \* )", que significa que você receberá notificações para alterações em qualquer objeto no escopo especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Atributos<br/> | Especifique uma lista de atributos para retornar quando ocorrer uma alteração. Lembre-se de receber notificações quando qualquer atributo for modificado, não apenas os atributos especificados.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

Você pode registrar até cinco solicitações de notificação em uma única conexão LDAP. Você deve ter um thread dedicado que aguarda as notificações e processa-as rapidamente. Quando você chama a \_ função ext de pesquisa LDAP \_ para registrar uma solicitação de notificação, a função retorna um identificador de mensagem que identifica essa solicitação. Em seguida, você usa a função de [**\_ resultado LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) para aguardar as notificações de alteração. Quando ocorre uma alteração, o servidor envia uma mensagem LDAP que contém o identificador da mensagem para a solicitação de notificação que gerou a notificação. Isso faz com que a função de **\_ resultado LDAP** seja retornada com os resultados da pesquisa que identificam o objeto que foi alterado.

O aplicativo cliente deve determinar o estado inicial do objeto monitorado. Para fazer isso, primeiro você deve registrar a solicitação de notificação e, em seguida, ler o estado atual.

O aplicativo cliente também deve determinar a causa da alteração. Para uma pesquisa de nível de base, uma notificação ocorre quando qualquer atributo é alterado ou quando o objeto é excluído ou movido. Para uma pesquisa de um nível, uma notificação ocorre quando um objeto filho é criado, excluído, movido ou modificado. Lembre-se de que mover ou renomear um objeto na hierarquia acima de um objeto de destino não gera uma notificação, embora o nome distinto do destino seja alterado como resultado. Por exemplo, se o monitoramento mudar para os objetos filho em um contêiner, você não receberá notificações se o próprio contêiner for movido ou renomeado.

Quando o cliente processa os resultados da pesquisa, ele pode usar a \_ função LDAP get \_ DN para obter o nome distinto do objeto que foi alterado. Não confie em nomes distintos para identificar os objetos rastreados, pois nomes distintos podem ser alterados. Em vez disso, inclua o atributo **objectGUID** na lista de atributos a serem recuperados. O **objectGUID** de cada objeto permanece inalterado, independentemente de onde o objeto é movido dentro da floresta da empresa.

Se um objeto dentro do escopo de pesquisa for excluído, o cliente receberá uma notificação de alteração e o atributo **IsDeleted** do objeto será definido como **true**. Nesse caso, os resultados da pesquisa relatam o novo nome distinto do objeto no contêiner objetos excluídos de sua partição. Não é necessário especificar o controle de marca de exclusão ([ \_ servidor LDAP \_ Mostrar \_ \_ OID excluído](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) para obter notificações de exclusões de objetos. Para obter mais informações, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).

Quando um cliente registra uma solicitação de notificação, o cliente continua a receber notificações até que a conexão seja interrompida ou o cliente abandone a pesquisa chamando a \_ função de Abandon LDAP. Se o cliente ou servidor se desconectar, por exemplo, se o servidor falhar, a solicitação de notificação será encerrada. Quando o cliente se reconecta, ele deve se registrar para notificações novamente e, em seguida, ler o estado atual dos objetos de interesse caso haja alterações enquanto o cliente estava desconectado.

O cliente pode usar o valor do atributo **uSNChanged** de um objeto para determinar se o estado atual do objeto no servidor reflete as alterações mais recentes que o cliente recebeu. O sistema aumenta o atributo **uSNChanged** de um objeto quando o objeto é movido ou modificado. Por exemplo, se o servidor falhar e a partição de diretório for restaurada de um backup, a réplica do servidor de um objeto poderá não refletir as alterações relatadas anteriormente para o cliente; nesse caso, o valor de **uSNChanged** no servidor será menor do que o valor armazenado pelo cliente.

Para obter mais informações e um exemplo de código que usa o controle de notificação de alteração LDAP em uma operação de pesquisa LDAP assíncrona, consulte o [código de exemplo para receber notificações de alteração](example-code-for-receiving-change-notifications.md).

Para obter mais informações sobre quando usar o controle de notificação de alteração de LDAP, consulte [visão geral das técnicas de controle de alterações](overview-of-change-tracking-techniques.md).

 

