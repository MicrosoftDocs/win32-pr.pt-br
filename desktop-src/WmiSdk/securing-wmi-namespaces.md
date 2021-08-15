---
description: O acesso a namespaces WMI e seus dados é controlado por descritores de segurança.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Proteger namespaces WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992366"
---
# <a name="securing-wmi-namespaces"></a>Proteger namespaces WMI

O acesso a namespaces WMI e seus dados é controlado [*por descritores de segurança*](gloss-s.md). Você pode proteger dados em [*seus namespaces*](gloss-n.md) ajustando o descritor de segurança do namespace para controlar quem tem acesso aos dados e métodos. Para obter mais informações, [consulte Access to WMI Securable Objects](access-to-wmi-securable-objects.md).


Os tópicos a seguir descrevem a segurança do namespace WMI e como controlar o acesso aos namespaces.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dd>

A segurança do namespace do WMI depende [](/windows/desktop/SecGloss/s-gly) de SIDs (identificadores de segurança de usuário) Windows padrão e listas de controle de acesso. Administradores e usuários têm permissões padrão diferentes.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Definindo descritores de segurança do namespace](setting-namespace-security-descriptors.md)
</dt> <dd>

Depois que um namespace existir no repositório WMI, você poderá alterar a segurança no namespace usando o Controle WMI ou chamando os métodos [**\_ \_ de SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

O **qualificador RequiresEncryption** em um namespace requer que o script ou o aplicativo cliente WMI use o nível de autenticação que criptografa chamadas de procedimento remoto. Solicitações de dados de entrada e retornos de chamada assíncronos devem ser criptografados.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mantendo a segurança WMI](maintaining-wmi-security.md)
</dt> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Criando um namespace com a API WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Objetos do descritor de segurança WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
