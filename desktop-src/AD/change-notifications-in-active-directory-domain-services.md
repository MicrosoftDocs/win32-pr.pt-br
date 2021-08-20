---
title: Alterar notificações no Active Directory Domain Services
description: Active Directory Domain Services um mecanismo para um aplicativo cliente se registrar com um controlador de domínio para receber notificações de alteração.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c224fd8910a127262bc8dc0839341f1c02c85ff0ac46045f31968795e2de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023127"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Alterar notificações no Active Directory Domain Services

Active Directory Domain Services um mecanismo para um aplicativo cliente se registrar com um controlador de domínio para receber notificações de alteração. Para fazer isso, o cliente especifica o controle de notificação de alteração LDAP em uma operação de pesquisa LDAP assíncrona. O cliente também especifica os seguintes parâmetros de pesquisa.



| Parâmetro             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escopo<br/>      | Especifique **LDAP \_ SCOPE \_ BASE** para monitorar apenas o objeto ou **LDAP \_ SCOPE \_ ONELEVEL** para monitorar os filhos imediatos do objeto, não incluindo o próprio objeto. Não especifique **LDAP \_ SCOPE \_ SUBTREE**. Embora o escopo da subárvore tenha suporte se o objeto base for a raiz de um contexto de nomengamento, seu uso pode afetar gravemente o desempenho do servidor, pois gera uma mensagem de resultado da pesquisa LDAP sempre que um objeto no contexto de nomen básico é modificado. Não é possível especificar **A \_ \_ SUBÁRVORE DE ESCOPO LDAP** para uma subárvore arbitrária.<br/> |
| Filtrar<br/>     | Especifique um filtro de pesquisa "(objectclass= )", o que significa que você recebe notificações para alterações em qualquer objeto \* no escopo especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Atributos<br/> | Especifique uma lista de atributos a retornar quando ocorrer uma alteração. Esteja ciente de que você recebe notificações quando qualquer atributo é modificado, não apenas os atributos especificados.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

Você pode registrar até cinco solicitações de notificação em uma única conexão LDAP. Você deve ter um thread dedicado que aguarde as notificações e processe-as rapidamente. Quando você chama a função ext de pesquisa ldap para registrar uma solicitação de notificação, a função retorna um identificador de mensagem \_ \_ que identifica essa solicitação. Em seguida, use a [**função de resultado ldap \_**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) para aguardar notificações de alteração. Quando ocorre uma alteração, o servidor envia uma mensagem LDAP que contém o identificador de mensagem para a solicitação de notificação que gerou a notificação. Isso faz com que **a função de \_ resultado ldap** retorne com resultados de pesquisa que identificam o objeto que foi alterado.

O aplicativo cliente deve determinar o estado inicial do objeto monitorado. Para fazer isso, você deve primeiro registrar a solicitação de notificação e, em seguida, ler o estado atual.

O aplicativo cliente também deve determinar a causa da alteração. Para uma pesquisa de nível base, ocorre uma notificação quando qualquer atributo é mudado ou quando o objeto é excluído ou movido. Para uma pesquisa de um nível, uma notificação ocorre quando um objeto filho é criado, excluído, movido ou modificado. Esteja ciente de que mover ou renomear um objeto na hierarquia acima de um objeto de destino não gera uma notificação, mesmo que o nome diferenciado do destino tenha mudado como resultado. Por exemplo, se o monitoramento mudar para os objetos filho em um contêiner, você não receberá notificações se o contêiner em si for movido ou renomeado.

Quando o cliente processa os resultados da pesquisa, ele pode usar a função ldap get dn para obter o nome diferenciado \_ do objeto que foi \_ alterado. Não confie em nomes diferenciados para identificar os objetos rastreados, pois nomes diferenciados podem mudar. Em vez disso, inclua **o atributo objectGUID** na lista de atributos a recuperar. O **objectGUID** de cada objeto permanece inalterado, independentemente de onde o objeto é movido dentro da floresta corporativa.

Se um objeto dentro do escopo de pesquisa for excluído, o cliente receberá uma notificação de alteração e o **atributo isDeleted** do objeto será definido como **TRUE.** Nesse caso, os resultados da pesquisa relatam o novo nome diferenciado do objeto no contêiner Objetos Excluídos de sua partição. Não é necessário especificar o controle de exclusão ([LDAP \_ SERVER \_ SHOW \_ DELETED \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) para obter notificações de exclusões de objeto. Para obter mais informações, [consulte Recuperando objetos excluídos.](retrieving-deleted-objects.md)

Quando um cliente tiver registrado uma solicitação de notificação, o cliente continuará recebendo notificações até que a conexão seja interrompida ou o cliente abandone a pesquisa chamando a função ldap \_ abandon. Se o cliente ou servidor se desconectar, por exemplo, se o servidor falhar, a solicitação de notificação será encerrada. Quando o cliente se reconecta, ele deve se registrar para notificações novamente e, em seguida, ler o estado atual dos objetos de interesse caso haja alterações enquanto o cliente foi desconectado.

O cliente pode usar o valor do atributo **uSNChanged** de um objeto para determinar se o estado atual do objeto no servidor reflete as alterações mais recentes recebidas pelo cliente. O sistema aumenta o atributo **uSNChanged** de um objeto quando o objeto é movido ou modificado. Por exemplo, se o servidor falhar e a partição de diretório for restaurada de um backup, a réplica do servidor de um objeto poderá não refletir as alterações relatadas anteriormente ao cliente, caso em que o valor **uSNChanged** no servidor será menor que o valor armazenado pelo cliente.

Para obter mais informações e um exemplo de código que usa o controle de notificação de alteração LDAP em uma operação de pesquisa LDAP assíncrona, consulte Código de exemplo para receber notificações [de alteração.](example-code-for-receiving-change-notifications.md)

Para obter mais informações sobre quando usar o controle de notificação de alteração LDAP, consulte Visão geral [Controle de Alterações técnicas de alteração.](overview-of-change-tracking-techniques.md)

 

