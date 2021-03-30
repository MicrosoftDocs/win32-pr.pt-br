---
title: Objetos dinâmicos
description: No Windows Server 2003 e versões posteriores do Windows, Active Directory Domain Services fornecer suporte para armazenar entradas dinâmicas no diretório.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- AD de objetos dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d521dabda8f82cbdcd46c00b3041f150f390d60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634971"
---
# <a name="dynamic-objects"></a>Objetos dinâmicos

No Windows Server 2003 e versões posteriores do Windows, Active Directory Domain Services fornecer suporte para armazenar entradas dinâmicas no diretório. Uma entrada dinâmica é um objeto no diretório que tem um valor de TTL (vida útil) associado. O TTL de uma entrada é definido quando a entrada é criada. A vida útil é automaticamente diminuída e quando ela expira a entrada dinâmica desaparece. O cliente pode fazer com que uma entrada dinâmica permaneça mais do que sua vida útil atual atualizando (modificando) seu valor de TTL. Os clientes que armazenam dados dinâmicos no diretório devem atualizar periodicamente esses dados para impedir que eles sejam desaparecedos.

Muitos aplicativos e serviços que usam o LDAP para armazenar e acessar dados relativamente estáticos e globalmente interessantes de um servidor de Active Directory também preferem continuar usando o acesso LDAP para suas necessidades de dados dinâmicos. Além disso, para alguns aplicativos, pode ser desejável descarregar a tarefa de objetos de coleta de lixo no DS que têm uma vida útil limitada para o serviço de diretório. As partições de diretório de aplicativo (com a capacidade de posicionamento controlado de réplicas) e de TTLs por objeto, juntas, fornecerão a capacidade de hospedar dados dinâmicos em Active Directory Domain Services, permitindo assim o acesso LDAP a ele.

Uma nova classe de objeto auxiliar chamada **DynamicObject** com OID = 1.3.6.1.4.1.1466.101.119.2 será definida no esquema de base do AD a ser usado por entradas dinâmicas. Essa classe auxiliar contém o atributo chamado **entryTTL** com OID = 1.3.6.1.4.1.1466.101.119.3 como um atributo System-Mai-contain. O valor desse atributo é o "tempo em segundos" que a entrada de diretório correspondente continuará existindo antes de desaparecer do diretório. Se o cliente não fornecer um valor para esse atributo explicitamente na criação do objeto, o DS fornecerá um valor padrão, conforme especificado posteriormente.

Uma nova operação LDAP estendida com OID = 1.3.6.1.4.1.1466.101.119.1 para a atualização de cliente de uma entrada dinâmica no diretório será definida e publicada no atributo **supportedExtension** do objeto DSE raiz.

Na implementação real, **entryTTL** é um atributo construído. O tempo de expiração real do objeto é armazenado como uma hora absoluta quando o objeto pode ser destruído em um atributo somente do sistema chamado **MS-DS-entry-time-to-Live**.

Todos os objetos dinâmicos têm as seguintes limitações:

-   Um objeto dinâmico excluído devido a seu TTL expirando não deixa uma marca para exclusão.
-   Todos os DCs que contêm réplicas de objetos dinâmicos devem ser executados no Windows Server 2003.
-   As entradas dinâmicas com valores de TTL têm suporte em todas as partições, exceto a partição de configuração e a partição de esquema.
-   Active Directory Domain Services não publique o atributo opcional **dynamicSubtrees** , conforme descrito no RFC 2589, no objeto raiz do dse.
-   As entradas dinâmicas são tratadas de forma semelhante a entradas não dinâmicas ao processar operações de pesquisa, comparação, adição, exclusão, modificação e modifyDN.
-   Não é possível alterar uma entrada estática para uma entrada dinâmica e vice-versa.
-   Uma entrada não dinâmica não pode ser adicionada subordinada a uma entrada dinâmica.

 

 




