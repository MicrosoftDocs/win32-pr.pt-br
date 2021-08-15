---
title: Objetos dinâmicos
description: No Windows Server 2003 e versões posteriores do Windows, o Active Directory Domain Services fornece suporte para armazenar entradas dinâmicas no diretório.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- AD de objetos dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191714"
---
# <a name="dynamic-objects"></a>Objetos dinâmicos

No Windows Server 2003 e versões posteriores do Windows, o Active Directory Domain Services fornece suporte para armazenar entradas dinâmicas no diretório. Uma entrada dinâmica é um objeto no diretório que tem um valor TTL (vida vida) associado. O TTL de uma entrada é definido quando a entrada é criada. O tempo de vida é automaticamente decrementado e, quando expira, a entrada dinâmica desaparece. O cliente pode fazer com que uma entrada dinâmica permaneça por mais tempo do que a vida restante atual, atualize (modificando) seu valor de TTL. Os clientes que armazenam dados dinâmicos no diretório devem atualizar periodicamente esses dados para impedir que eles desapareçam.

Muitos aplicativos e serviços que usam lDAP para armazenar e acessar dados relativamente estáticos e globalmente interessantes de um servidor do Active Directory também preferem continuar usando o acesso LDAP para suas necessidades de dados dinâmicos. Além disso, para alguns aplicativos, pode ser desejável o descarramento da tarefa de coleta de lixo de objetos no DS que têm uma vida útil limitada para o serviço de diretório. As partições do diretório do aplicativo (com a capacidade de posicionamento controlado de réplicas) e as TTLs por objeto juntas fornecerão a capacidade de hospedar dados dinâmicos no Active Directory Domain Services, permitindo assim o acesso LDAP a eles.

Uma nova classe de objeto auxiliar chamada **dynamicObject** com OID = 1.3.6.1.4.1.1466.101.119.2 será definida no esquema base do AD a ser usado por entradas dinâmicas. Essa classe auxiliar contém o atributo chamado **entryTTL** com OID = 1.3.6.1.4.1.1466.101.119.3 como um atributo system-may-contain. O valor desse atributo é o "tempo em segundos" que a entrada de diretório correspondente continuará a existir antes de desaparecer do diretório. Se o cliente não fornecer um valor para esse atributo explicitamente na criação do objeto, o DS fornecerá um valor padrão, conforme especificado posteriormente.

Uma nova operação LDAP estendida com OID = 1.3.6.1.4.1.1466.101.119.1 para atualização do cliente de uma entrada dinâmica no diretório será definida e publicada no atributo **supportedExtension** do objeto DSE raiz.

Na implementação real, **entryTTL** é um atributo construído. O tempo de expiração real do objeto é armazenado como um tempo absoluto em que o objeto pode ser destruído em um atributo somente do sistema chamado **ms-DS-Entry-Time-To-Live.**

Todos os objetos dinâmicos têm as seguintes limitações:

-   Um objeto dinâmico excluído devido à sua expiração de TTL não deixa uma chave de exclusão para trás.
-   Todos os DCs que têm réplicas de objetos dinâmicos devem ser executados Windows Server 2003.
-   Há suporte para entradas dinâmicas com valores TTL em todas as partições, exceto a partição De configuração e a partição de esquema.
-   Active Directory Domain Services não publique o atributo **opcional dynamicSubtrees,** conforme descrito no RFC 2589, no objeto DSE raiz.
-   Entradas dinâmicas são tratadas de forma semelhante a entradas não dinâmicas ao processar operações search, compare, add, delete, modify e modifyDN.
-   Não há como alterar uma entrada estática em uma entrada dinâmica e vice-versa.
-   Uma entrada não dinâmica não pode ser adicionada subordinada a uma entrada dinâmica.

 

 




