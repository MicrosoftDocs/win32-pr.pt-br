---
description: O WMI tem objetos e métodos que permitem ler e manipular descritores de segurança para determinar quem tem acesso a objetos protegíveis.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objetos do descritor de segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551353"
---
# <a name="wmi-security-descriptor-objects"></a>Objetos do descritor de segurança do WMI

O WMI tem objetos e métodos que permitem ler e manipular descritores de segurança para determinar quem tem acesso a objetos protegíveis.

-   [A função de descritores de segurança](#the-role-of-security-descriptors)
-   [Controle de acesso e objetos de segurança do WMI](#access-control-and-wmi-security-objects)
-   [\_Objeto SecurityDescriptor do Win32](/windows)
-   [DACL e SACL](#dacl-and-sacl)
-   [Win32 \_ Ace, confiança do Win32 \_ , \_ SID do Win32](/windows)
-   [Exemplo: verificando quem tem acesso às impressoras](#example-checking-who-has-access-to-printers)
-   [Tópicos relacionados](#related-topics)

## <a name="the-role-of-security-descriptors"></a>A função de descritores de segurança

Os descritores de segurança definem os atributos de segurança de objetos protegíveis, como arquivos, chaves do registro, namespaces do WMI, impressoras, serviços ou compartilhamentos. Um descritor de segurança contém informações sobre o proprietário e o grupo primário de um objeto. Um provedor pode comparar o descritor de segurança de recurso com a identidade de um usuário solicitante e determinar se o usuário tem o direito de acessar o recurso que um usuário está solicitando. Para obter mais informações, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).

Alguns métodos [**WMI, como o obtido**](--systemsecurity-getsd.md), retornam um descritor de segurança no formato de matriz de bytes binários. A partir do Windows Vista, use os métodos da classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para converter um descritor de segurança binário em uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), que pode ser manipulada com mais facilidade. Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Controle de acesso e objetos de segurança do WMI

A seguir está uma lista de objetos de segurança do WMI:

-   [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**Confiança do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**Sid do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

O diagrama a seguir mostra as relações entre os objetos de segurança do WMI.

![relações entre os objetos de segurança do WMI](images/security-descriptor.png)

Para obter mais informações sobre a função de segurança de acesso, consulte [práticas recomendadas de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis), [mantendo a segurança do WMI](maintaining-wmi-security.md)e o controle de [acesso](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>\_Objeto SecurityDescriptor do Win32

A tabela a seguir lista as propriedades da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .



| Propriedade         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Conjunto de bits de controle que qualifica o significado de um SD ou de seus membros individuais. Para obter mais informações sobre como definir os valores de bit **ControlFlags** , consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | [Lista de controle de acesso discricional (ACL)](/windows/desktop/SecAuthZ/access-control-lists) de usuários e grupos e seus direitos de acesso a um objeto protegido. Essa propriedade contém uma matriz de instâncias do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representam [entradas de controle de acesso](/windows/desktop/SecAuthZ/access-control-entries). Para obter mais informações, consulte [criando uma DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Grupo**        | Grupo ao qual este objeto protegido pertence. Essa propriedade contém uma instância de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contém o nome, o domínio e o Sid (identificador de segurança) do grupo ao qual o proprietário pertence.<br/>                                                                                                                                                             |
| **Proprietário**        | Proprietário deste objeto protegido. Essa propriedade contém uma instância de [ \_ confiança do Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contém o nome, o domínio e o Sid (identificador de segurança) do proprietário.<br/>                                                                                                                                                                                                          |
| **Right**         | A [ACL (lista de controle de acesso) do sistema](/windows/desktop/SecAuthZ/access-control-lists) contém uma matriz de instâncias do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representam o tipo de tentativas de acesso que geram registros de auditoria para usuários ou grupos. Para obter mais informações, consulte [SACL para um novo objeto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL e SACL

As matrizes de objetos do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) na DACL (lista de controle de acesso discricionário) e na lista de controle de acesso do sistema {SACL) criam um vínculo entre um usuário ou grupo e seus direitos de acesso.

Quando uma propriedade DACL não contém uma ACE (entrada de controle de acesso), os direitos de acesso não são concedidos e o acesso ao objeto é negado.

> [!Note]  
> Uma DACL **nula** dá acesso completo a todos, o que é um risco de segurança sério. Para obter mais informações, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>Win32 \_ Ace, confiança do Win32 \_ , \_ SID do Win32

Um objeto do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contém uma instância da classe de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que identifica um usuário ou grupo e uma propriedade **AccessMask** que é um bitmask, que especifica as ações que um usuário ou grupo pode executar. Por exemplo, um usuário ou grupo pode receber o direito de ler um arquivo, mas não gravar no arquivo. Um objeto do **Win32 \_ Ace** também contém uma ACE que indica se é ou não um acesso de permissão ou negação.

> [!Note]  
> A ordem de [**\_ Ace do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) em uma DACL é importante porque permitir e negar entrada de controle de acesso (ACE) são permitidos em uma DACL. Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Cada conta de usuário ou grupo representado por [**um \_ confiável do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) tem um SID (identificador de segurança) que identifica exclusivamente uma conta e especifica os privilégios de acesso da conta. A maneira como você especifica os dados do SID depende do sistema operacional. Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

O diagrama a seguir mostra o conteúdo de uma instância do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

![conteúdo de uma instância do Win32 \- Ace](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Exemplo: verificando quem tem acesso às impressoras

O exemplo de código VBScript a seguir mostra como usar o descritor de segurança da impressora. O script chama o método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) na classe [**de \_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) para obter o descritor e determina se há uma DACL (lista de controle de acesso discricionário) presente no descritor de segurança. Se houver uma DACL, o script obterá a lista de entradas de controle de acesso (ACE) da DACL. Cada ACE é representado por uma instância do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). O script verifica cada ACE para obter o nome do usuário e determinar se o usuário tem acesso à impressora. O usuário é representado por uma instância do [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) inserido na instância do **Win32 \_ Ace** .


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md)
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

 

