---
description: a partir do Windows Vista, muitos objetos protegíveis têm métodos para obter ou definir o descritor de segurança. Com as permissões apropriadas, você pode ler ou alterar descritores de segurança em objetos protegíveis.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Alterando a segurança de acesso em objetos protegíveis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050984"
---
# <a name="changing-access-security-on-securable-objects"></a>Alterando a segurança de acesso em objetos protegíveis

Impressoras, serviços, chaves do registro, aplicativos DCOM e namespaces do WMI são objetos protegíveis. O acesso a objetos protegíveis é protegido por [*descritores de segurança*](/windows/desktop/SecGloss/s-gly), que especificam os usuários que têm acesso. a partir do Windows Vista, muitos objetos protegíveis têm métodos para obter ou definir o descritor de segurança. Com as permissões apropriadas, você pode ler ou alterar descritores de segurança em objetos protegíveis. Usando esses métodos, você pode controlar quais contas de usuário ou grupos têm acesso a uma impressora, serviço, namespace WMI ou outro objeto. Para obter mais informações sobre descritores de segurança e seu uso no WMI, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).

As seções a seguir são discutidas neste tópico:

-   [Objetos e métodos de descritor de segurança](#objects-and-security-descriptor-methods)
-   [Convertendo entre formatos de descritor de segurança](#converting-between-security-descriptor-formats)
-   [Problemas de segurança](#security-issues)
-   [Tópicos relacionados](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Objetos e métodos de descritor de segurança

A lista a seguir contém os métodos que os objetos protegíveis têm para permitir que você leia ou altere o descritor de segurança:

-   Namespaces WMI

    Um provedor pode estabelecer a segurança que só permite que determinados grupos tenham acesso aos dados em um namespace WMI. A segurança do namespace é controlada por métodos na classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . a partir do Windows Vista, os métodos [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) retornam e gravam objetos [**\_ \_ SecurityDescriptor**](--securitydescriptor.md) . Para obter mais informações, consulte [Configurando descritores de segurança de namespace](setting-namespace-security-descriptors.md).

-   Chaves do Registro

    a partir do Windows Vista, você pode proteger as chaves do registro para que elas não possam ser alteradas por usuários não autorizados. A classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tem os métodos [**GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) . Esses métodos retornam e gravam objetos [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Impressoras

    a partir do Windows Vista, você pode proteger o acesso a instâncias da classe de [**\_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) usando os métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) . Esses métodos retornam e gravam objetos [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Serviços

    a partir do Windows Vista, você pode proteger o acesso a instâncias da classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) usando os métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) . Esses métodos retornam e gravam objetos [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Aplicativos DCOM

    As instâncias do aplicativo DCOM têm vários descritores de segurança. a partir do Windows Vista, use métodos da classe [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) para obter ou alterar os vários descritores de segurança. Descritores de segurança são retornados como instâncias da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

    Para obter ou alterar as permissões de configuração, chame os métodos [**GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ou [**SetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Para obter ou alterar as permissões de acesso, chame os métodos [**GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ou [**SetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Para obter ou alterar as permissões de inicialização e ativação, chame os métodos [**GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) ou [**SetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ,

-   Arquivos

    Os métodos [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) estão na classe [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) , em vez de na classe de [**DataFile do \_ arquivo CIM**](/windows/desktop/CIMWin32Prov/cim-datafile) .

-   Compartilhamentos

    Os métodos [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) e [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) estão na classe [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) , em vez de na classe [**de \_ compartilhamento Win32**](/windows/desktop/CIMWin32Prov/win32-share) .

> [!Note]  
> Quando uma nova [*SACL (lista de controle de acesso de segurança)*](/windows/desktop/SecGloss/s-gly) não é especificada em uma chamada para um método **SETSECURITYDESCRIPTOR** , a SACL do descritor de segurança no objeto protegível de destino é definida como **NULL** para que a configuração SACL anterior não persista.

 

## <a name="converting-between-security-descriptor-formats"></a>Convertendo entre formatos de descritor de segurança

Descritores de segurança são matrizes de bytes binários complexos que normalmente devem ser criadas e alteradas em C++. Depois de ter usado um dos métodos get para obter o descritor de segurança, a classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) fornece métodos que convertem descritores de segurança em uma [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ou em instâncias do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

Você pode manipular as listas de controle de acesso (ACL) mais facilmente em instâncias [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou em SDDL. Para obter mais informações sobre a estrutura e o uso de descritores de segurança no WMI, consulte [objetos de descrição do WMI Security](wmi-security-descriptor-objects.md).

Em C++ ou C#, use funções de conversão para converter descritores de segurança binários em [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Para modificar os valores do descritor de segurança em aplicativos C++, use [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Problemas de segurança

É recomendável que as alterações nos descritores de segurança sejam feitas com muito cuidado para que a segurança do objeto não seja comprometida. Lembre-se de que a ordem das ACEs (entradas de controle de acesso) em uma DACL (lista de controle de acesso discricionário) pode afetar a segurança do acesso. Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Classe auxiliar do descritor de segurança](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Práticas recomendadas de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> <dt>

[Controle de acesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
