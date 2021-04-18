---
description: Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Estabelecendo a herança da segurança do namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796177"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Estabelecendo a herança da segurança do namespace

Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.

Os namespaces WMI têm descritores de segurança que controlam quem pode acessar o namespace e os dados do namespace. Cada descritor de segurança tem uma DACL (lista de controle de acesso discricionário) e uma SACL (lista de controle de acesso de segurança). Essas listas contêm entradas de controle de acesso (ACE).

Dependendo das constantes do [**sinalizador Ace do namespace**](namespace-ace-flag-constants.md) que são definidas, as permissões que são aplicadas a um namespace podem ser herdadas por todos os namespaces filho desse namespace. Um namespace filho herda o descritor de segurança de seu namespace pai quando o namespace filho é criado se o **contêiner \_ herdar \_** o sinalizador Ace está no descritor de segurança do namespace pai. Se **contêiner \_ herdar Ace \_ \| não \_ se propagar \_ herdar \_ Ace** está definido, somente o namespace filho herdará o descritor de segurança, não os namespaces do neto. Os namespaces filho podem substituir as permissões de segurança de seu pai chamando métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) para gravar um novo descritor de segurança. As configurações de segurança padrão não podem ser alteradas. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md). Para obter mais informações sobre DACLs, consulte as constantes [ACLs (listas de controle de acesso)](/windows/desktop/SecAuthZ/access-control-lists) e [**tipo de ACE de namespace**](namespace-ace-type-constants.md).

Observe que as permissões padrão não podem ser alteradas. Além disso, a configuração do sinalizador **se \_ \_ protegido por DACL** ao definir o descritor de segurança (SD) não é usada para adicionar um SD especializado a um namespace filho. Para substituir um SD herdado, basta definir um novo. Para herdar o SD para um namespace filho, passe o sinalizador **\_ \_ Ace Inherit do contêiner** no descritor de segurança do namespace. Para herdar apenas o filho, e não os descendentes, passe `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
