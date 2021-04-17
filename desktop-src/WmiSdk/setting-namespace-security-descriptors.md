---
description: Tanto os aplicativos C++ quanto os scripts em execução com uma conta de administrador completo podem alterar um descritor de segurança de namespace.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Definindo descritores de segurança de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762433"
---
# <a name="setting-namespace-security-descriptors"></a>Definindo descritores de segurança de namespace

Tanto os aplicativos C++ quanto os scripts em execução com uma conta de administrador completo podem alterar um descritor de segurança de namespace.

## <a name="namespace-security-descriptors"></a>Descritores de segurança de namespace

Cada namespace WMI tem um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly), que permite que cada namespace tenha configurações de segurança exclusivas que determinam quem tem acesso aos dados e métodos do namespace. Para obter mais informações sobre a segurança de acesso do WMI, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md). O [acesso aos namespaces do WMI](access-to-wmi-namespaces.md) descreve as configurações de segurança padrão para namespaces do WMI e auditoria de segurança no WMI.

Você pode definir permissões de conta para cada namespace WMI no repositório WMI (CIM) das seguintes maneiras:

-   Quando o namespace é criado no arquivo MOF. Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).
-   Manualmente, usando o controle WMI. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).
-   Programaticamente, chamando os métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .

Os métodos a seguir do objeto [**\_ \_ SystemSecurity**](--systemsecurity.md) associado a cada namespace permitem que você leia ou altere a segurança em um namespace.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Define o parâmetro de *direitos* como um bitmap com cada bit correspondente a um direito de acesso.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Obtém o descritor de segurança para o namespace ao qual o usuário está conectado. Esse método retorna um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Define o descritor de segurança (SD) para o namespace ao qual um usuário está conectado. Esse método requer um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Obtém o descritor de segurança que controla o acesso ao namespace WMI associado à instância de [**\_ \_ SystemSecurity**](--systemsecurity.md). O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora. O descritor de segurança é representado por uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Define os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.

</dd> </dl>

Se você estiver escrevendo scripts, use o [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e o [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md). Você pode usar os métodos da classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para alterar os descritores de segurança.

Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando o [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Lembre-se de que, a partir do Windows Vista, o UAC ( [controle de conta de usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ) afeta o acesso aos dados do WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md). Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
