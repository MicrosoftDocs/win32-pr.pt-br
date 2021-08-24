---
description: Tanto aplicativos C++ quanto scripts em execução em uma conta de administrador completo podem alterar um descritor de segurança de namespace.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Definindo descritores de segurança do namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc112376a960c3760bc51450cc30b8da3a38c24fa52e985321b2662ae319a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050294"
---
# <a name="setting-namespace-security-descriptors"></a>Definindo descritores de segurança do namespace

Tanto aplicativos C++ quanto scripts em execução em uma conta de administrador completo podem alterar um descritor de segurança de namespace.

## <a name="namespace-security-descriptors"></a>Descritores de segurança do namespace

Cada namespace WMI tem um descritor [*de*](/windows/desktop/SecGloss/s-gly)segurança , que permite que cada namespace tenha configurações de segurança exclusivas que determinam quem tem acesso aos dados e métodos do namespace. Para obter mais informações sobre a segurança de acesso do WMI, consulte [Acesso a objetos de segurança WMI.](access-to-wmi-securable-objects.md) [O acesso a namespaces WMI](access-to-wmi-namespaces.md) descreve as configurações de segurança padrão para namespaces WMI e auditoria de segurança no WMI.

Você pode definir permissões de conta para cada namespace WMI no repositório CIM (WMI) das seguintes maneiras:

-   Quando o namespace é criado no arquivo MOF. Para obter mais informações, consulte [Configurando a segurança do namespace quando o namespace é criado.](setting-namespace-security-when-the-namespace-is-created.md)
-   Manualmente, usando o controle WMI. Para obter mais informações, consulte [Configurando a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).
-   Programaticamente, chamando os métodos da [**\_ \_ classe SystemSecurity.**](--systemsecurity.md)

Os métodos a seguir do objeto [**\_ \_ SystemSecurity**](--systemsecurity.md) associados a cada namespace permitem que você leia ou altere a segurança em um namespace.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Define o *parâmetro rights* como um bitmap com cada bit correspondente a um direito de acesso.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Obtém o descritor de segurança para o namespace ao qual o usuário está conectado. Esse método retorna um descritor de segurança no formato de matriz de byte binário. Se você estiver escrevendo um script, use o [**método GetSecurityDescriptor.**](getsecuritydescriptor-method-in-class---systemsecurity-.md)

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Define o SD (descritor de segurança) para o namespace ao qual um usuário está conectado. Esse método requer um descritor de segurança no formato de matriz de byte binário. Se você estiver escrevendo um script, use o [**método SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md)

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Obtém o descritor de segurança que controla o acesso ao namespace WMI associado à instância do [**\_ \_ SystemSecurity**](--systemsecurity.md). O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora. O descritor de segurança é representado por uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio Windows descritores de segurança não está disponível.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Define os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio Windows descritores de segurança não está disponível.

</dd> </dl>

Se você estiver escrevendo scripts, use [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md). Você pode usar os métodos da classe [**\_ Win32 SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para alterar os descritores de segurança.

Se você estiver programando no C++, poderá manipular o descritor de segurança binária usando a [SDDL (Linguagem](/windows/desktop/SecAuthZ/security-descriptor-definition-language)de Definição do Descritor de Segurança) e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Esteja ciente de que, a partir do Windows [Vista,](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) o UAC (Controle de Conta de Usuário) afeta o acesso aos dados do WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md). Para obter mais informações, consulte [Controle de conta de usuário e WMI](user-account-control-and-wmi.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Proteger namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de segurança WMI](wmi-security-constants.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos do descritor de segurança WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
