---
description: O WMI conta com os descritores de segurança padrão do Windows para controlar e proteger o acesso a objetos protegíveis, como namespaces, impressoras, serviços e aplicativos DCOM do WMI.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Acesso a objetos protegíveis do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171460"
---
# <a name="access-to-wmi-securable-objects"></a>Acesso a objetos protegíveis do WMI

O WMI conta com os [*descritores de segurança*](/windows/desktop/SecGloss/s-gly) padrão do Windows para controlar e proteger o acesso a objetos protegíveis, como namespaces, impressoras, serviços e aplicativos DCOM do WMI. Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).

Os seguintes tópicos são discutidos nesta seção:

-   [Descritores de segurança e SIDs](#security-descriptors-and-sids)
-   [Controle de acesso](#access-control)
-   [Alterando a segurança de acesso](#changing-access-security)
-   [Tópicos relacionados](#related-topics)

## <a name="security-descriptors-and-sids"></a>Descritores de segurança e SIDs

O WMI mantém a segurança de acesso comparando o [*token de acesso*](/windows/desktop/SecGloss/a-gly) do usuário que tenta acessar um objeto protegível com o descritor de segurança do objeto.

Quando um usuário ou grupo é criado em um sistema, a conta recebe um [*Sid (identificador de segurança)*](/windows/desktop/SecGloss/s-gly) . o Sid garante que uma conta criada com o mesmo nome que uma conta excluída anteriormente não herde as configurações de segurança anteriores. Um token de acesso é criado pela combinação do SID, a lista de grupos dos quais o usuário é membro e a lista de privilégios habilitados ou desabilitados. Esses tokens são atribuídos a todos os processos e threads pertencentes ao usuário.

## <a name="access-control"></a>Controle de acesso

Quando o usuário quiser usar um objeto protegido, o token de acesso será comparado com a [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) no descritor de segurança do objeto. A DACL contém permissões chamadas [*de ACE (entradas de controle de acesso)*](/windows/desktop/SecGloss/a-gly). As [*listas de controle de acesso do sistema (SACL)*](/windows/desktop/SecGloss/s-gly) fazem a mesma coisa que as DACLs, mas podem gerar eventos de auditoria de segurança. A partir do Windows Vista, o WMI pode fazer entradas de auditoria no log de segurança do Windows. Para obter mais informações sobre auditoria no WMI, consulte [acesso aos namespaces do WMI](access-to-wmi-namespaces.md).

A DACL e a SACL consistem em uma lista de ACEs que descrevem quais usuários têm direitos de acesso específicos, incluindo gravação no repositório WMI, acesso remoto e execução e permissões de logon. O WMI armazena essas ACLs no repositório do WMI.

As ACEs contêm três tipos de níveis de acesso ou concedem/negam direitos: permitir, negar para DACL e auditoria do sistema (para SACLs). Deny ACEs precedem permitir ACEs na DACL ou SACL. Ao verificar os direitos de acesso do usuário, o WMI é executado consecutivamente por meio da lista de controle de acesso até encontrar uma ACE allow que se aplique ao token de acesso solicitante. As ACEs restantes não são verificadas após esse ponto. Se nenhum ACE de permissão apropriado for encontrado, o acesso será negado. Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) e [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Alterando a segurança de acesso

Com as permissões apropriadas, você pode alterar a segurança em um objeto protegível com um script ou aplicativo. Você também pode alterar as configurações de segurança nos namespaces do WMI usando o [*controle WMI*](gloss-w.md) ou adicionando uma cadeia de caracteres [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) no arquivo [*formato MOF (MOF)*](gloss-m.md) que define classes para o namespace. Para obter mais informações, consulte [acesso a namespaces do WMI](access-to-wmi-namespaces.md), [proteção de namespaces do WMI](securing-wmi-namespaces.md)e [alteração da segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Controle de conta de usuário e WMI](user-account-control-and-wmi.md)
</dt> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
