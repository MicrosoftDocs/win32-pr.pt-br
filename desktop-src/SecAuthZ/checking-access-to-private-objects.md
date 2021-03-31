---
description: Um aplicativo de servidor protegido deve verificar os direitos de acesso de clientes antes de permitir que o cliente acesse um objeto particular protegido.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Verificando o acesso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920991"
---
# <a name="checking-access-to-private-objects"></a>Verificando o acesso a objetos privados

Um aplicativo de servidor protegido deve verificar os direitos de acesso de um cliente antes de permitir que o cliente acesse um objeto particular protegido. Para fazer isso, o servidor passa um [*token de representação*](/windows/desktop/SecGloss/i-gly), um descritor de segurança e um conjunto de direitos de acesso solicitados para [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). As ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL [*do descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificam os direitos de acesso permitidos ou negados a vários itens confiáveis. A função **AccessCheck** compara o confiável em cada ACE com os confiáveis identificados no token de representação. Para obter uma descrição do algoritmo usado para conceder ou negar acesso, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).

A função [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) executa uma verificação de acesso semelhante. Além disso, ele gera registros de auditoria no log de eventos de segurança, dependendo da SACL no descritor de segurança.

As funções [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) e [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) são semelhantes a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , exceto que permitem que você verifique o acesso aos subobjetos de um objeto, como conjuntos de propriedades ou propriedades. As funções [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) e [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) também são semelhantes a **AccessCheck** , exceto que fornecem os resultados da verificação de acesso para cada subobjeto em uma hierarquia das propriedades e dos conjuntos de propriedades do objeto. Essas funções usam a estrutura da [**\_ \_ lista de tipos de objetos**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) para descrever a hierarquia de objetos para os quais o acesso está marcado. As funções que geram uma mensagem de auditoria usam o tipo de enumeração de [**\_ \_ tipo de evento Audit**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) para indicar se o objeto que está sendo verificado é um objeto de serviço de diretório. Para obter mais informações sobre a hierarquia de um objeto e seus subobjetos, consulte [ACEs para controlar o acesso às propriedades de um objeto](aces-to-control-access-to-an-object-s-properties.md).

Os direitos de acesso solicitados passados para as funções [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) não devem incluir nenhum [direito de acesso genérico](generic-access-rights.md). O servidor pode usar a função [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) para converter qualquer direito de acesso genérico aos direitos específicos e padrão correspondentes, de acordo com o mapeamento especificado na estrutura de [**\_ mapeamento genérico**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

As funções [**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) e [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) comparam uma [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) solicitada com uma máscara de acesso concedida.

Para obter o código de exemplo que usa a função [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , consulte [verificando o acesso do cliente com ACLs em C++](verifying-client-access-with-acls-in-c--.md).

A função [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) cria e retorna um descritor de segurança em um formato que permite a propagação automática de ACEs herdáveis. Este descritor de segurança contém todas as ACEs, herdadas e não herdadas, no descritor de segurança atual e está em formato [*auto-relativo*](/windows/desktop/SecGloss/s-gly) . A função **ConvertToAutoInheritPrivateObjectSecurity** determina se as ACEs são herdadas ou não herdadas, comparando todas as ACEs no descritor de segurança atual com todas as ACEs em seu descritor de segurança pai. Pode não haver uma correspondência um-para-um entre os dois grupos de ACEs. Por exemplo, uma ACE que permite permissão de leitura/gravação pode ser equivalente a duas ACEs: uma ACE que permite a permissão de leitura e uma ACE que permite a permissão de gravação. Um descritor de segurança pai não pode ser fornecido quando o descritor de segurança atual é o pai.

 

 
