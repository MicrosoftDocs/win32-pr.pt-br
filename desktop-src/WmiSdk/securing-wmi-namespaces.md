---
description: O acesso aos namespaces do WMI e seus dados são controlados por descritores de segurança.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Protegendo namespaces WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811718"
---
# <a name="securing-wmi-namespaces"></a>Protegendo namespaces WMI

O acesso aos namespaces do WMI e seus dados são controlados por [*descritores de segurança*](gloss-s.md). Você pode proteger dados em seus [*namespaces*](gloss-n.md) ajustando o descritor de segurança do namespace para controlar quem tem acesso aos dados e métodos. Para obter mais informações, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).


Os tópicos a seguir descrevem a segurança do namespace do WMI e como controlar o acesso a namespaces.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dd>

A segurança do namespace do WMI depende de SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) de usuário do Windows e listas de controle de acesso. Administradores e usuários têm permissões padrão diferentes.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Definindo descritores de segurança de namespace](setting-namespace-security-descriptors.md)
</dt> <dd>

Depois que um namespace existir no repositório do WMI, você poderá alterar a segurança no namespace usando o controle WMI ou chamando os métodos de [**\_ \_ SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

O qualificador **RequiresEncryption** em um namespace requer que o aplicativo cliente WMI ou o script use o nível de autenticação que criptografa chamadas de procedimento remoto. As solicitações de dados de entrada e os retornos de chamada assíncronos devem ser criptografados.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Criando um namespace com a API do WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
