---
description: Conjunto de sinalizadores de bits que qualificam o significado de um descritor de segurança ou seus componentes.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749217"
---
# <a name="security_descriptor_control"></a>\_controle do descritor de segurança \_

O tipo de dados de **\_ \_ controle do descritor de segurança** é um conjunto de sinalizadores de bits que qualificam o significado de um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) ou seus componentes. Cada descritor de segurança tem um membro de **controle** que armazena os bits de **\_ \_ controle do descritor de segurança** .


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Comentários

Para obter os bits de controle de um descritor de segurança, chame a função [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Para definir os bits de controle de um descritor de segurança, use as funções para modificar descritores de segurança. Para obter uma lista dessas funções, consulte a seção Consulte também.

Os aplicativos podem usar a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) para definir os bits de controle relacionados à herança automática de ACEs.

O valor de controle recuperado pela função [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) pode incluir uma combinação dos sinalizadores de bit de **\_ \_ controle do descritor de segurança** a seguir.



| Valor                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_req de \_ \_ herança automática \_ do se DACL<br/> 0x0100<br/> | Indica um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) necessário no qual a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) é configurada para dar suporte à propagação automática de ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) herdáveis para objetos filho existentes.<br/> Para [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACLs) que dão suporte à herança automática, esse bit é sempre definido. Os servidores protegidos podem chamar a função [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para converter um descritor de segurança e definir esse sinalizador. <br/> |
| \_autoria do se DACL \_ \_ herdado<br/> 0x0400<br/>    | Indica um descritor de segurança no qual a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) é configurada para dar suporte à propagação automática de ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) herdáveis para objetos filho existentes.<br/> Para [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACLs) que dão suporte à herança automática, esse bit é sempre definido. Os servidores protegidos podem chamar a função [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) para converter um descritor de segurança e definir esse sinalizador. <br/>                                                                                                  |
| \_padrão de DACL de se \_<br/> 0x0008<br/>          | Indica um descritor de segurança com uma DACL padrão. Por exemplo, se o criador de um objeto não especificar uma DACL, o objeto receberá a DACL padrão do [*token de acesso*](/windows/desktop/SecGloss/a-gly) do criador. Esse sinalizador pode afetar como o sistema trata a DACL com relação à herança de ACE. O sistema ignora esse sinalizador se o sinalizador SE a \_ DACL \_ presente não estiver definido.<br/> Esse sinalizador é usado para determinar como a DACL final no objeto deve ser computada e não é armazenada fisicamente no controle do descritor de segurança do objeto protegível.<br/> Para definir esse sinalizador, use a função [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| \_DACL \_ presente<br/> 0x0004<br/>            | Indica um descritor de segurança que tem uma DACL. Se esse sinalizador não estiver definido ou se esse sinalizador for definido e a DACL for **nula**, o descritor de segurança permitirá acesso completo a todos.<br/> Esse sinalizador é usado para manter as informações de segurança especificadas por um chamador até que o descritor de segurança seja associado a um objeto protegível. Depois que o descritor de segurança é associado a um objeto protegível, o sinalizador SE a \_ DACL \_ presente é sempre definido no controle do descritor de segurança.<br/> Para definir esse sinalizador, use a função [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| DACL de SE \_ \_ protegida<br/> 0x1000<br/>          | Impede que a DACL do descritor de segurança seja modificada por ACEs herdáveis. Para definir esse sinalizador, use a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_padrão do grupo se \_<br/> 0x0002<br/>         | Indica que o [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) (SID) do grupo de descritores de segurança foi fornecido por um mecanismo padrão. Esse sinalizador pode ser usado por um Gerenciador de recursos para identificar objetos cujo grupo de descritores de segurança foi definido por um mecanismo padrão. Para definir esse sinalizador, use a função [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_padrão do proprietário do se \_<br/> 0x0001<br/>         | Indica que o SID do proprietário do descritor de segurança foi fornecido por um mecanismo padrão. Esse sinalizador pode ser usado por um Gerenciador de recursos para identificar objetos cujo proprietário foi definido por um mecanismo padrão. Para definir esse sinalizador, use a função [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_controle RM \_ se \_ válido<br/> 0x4000<br/>       | Indica que o controle do Gerenciador de recursos é válido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_req. \_ \_ herança automática da SACL \_<br/> 0x0200<br/> | Indica um descritor de segurança necessário no qual a SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema é configurada para dar suporte à propagação automática de ACEs herdáveis para objetos filho existentes.<br/> O sistema define esse bit quando ele executa o algoritmo de herança automática para o objeto e seus objetos filho existentes. Para converter um descritor de segurança e definir esse sinalizador, os servidores protegidos podem chamar a função [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) .<br/>                                                                                                                                                                                                                                                                                   |
| \_ \_ auto \_ herdado do se SACL<br/> 0x0800<br/>    | Indica um descritor de segurança no qual a SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema é configurada para dar suporte à propagação automática de ACEs herdáveis para objetos filho existentes.<br/> O sistema define esse bit quando ele executa o algoritmo de herança automática para o objeto e seus objetos filho existentes. Para converter um descritor de segurança e definir esse sinalizador, os servidores protegidos podem chamar a função [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) . <br/>                                                                                                                                                                                                                                                                                           |
| \_definição de SACL \_ padrão<br/> 0x0008<br/>          | Um mecanismo padrão, em vez do [*provedor*](/windows/desktop/SecGloss/p-gly) original do descritor de segurança, forneceu a SACL. Esse sinalizador pode afetar como o sistema trata a SACL, com relação à herança de ACE. O sistema ignora esse sinalizador se o sinalizador da \_ SACL \_ presente não estiver definido. Para definir esse sinalizador, use a função [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_SACL \_ presente<br/> 0x0010<br/>            | Indica um descritor de segurança que tem uma SACL. Para definir esse sinalizador, use a função [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_SACL \_ protegida<br/> 0x2000<br/>          | Impede que a SACL do descritor de segurança seja modificada por ACEs herdáveis. Para definir esse sinalizador, use a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ auto \_ Relative<br/> 0x8000<br/>           | Indica um [*descritor de segurança auto-relativo*](/windows/desktop/SecGloss/s-gly). Se esse sinalizador não for definido, o descritor de segurança estará em formato absoluto. Para obter mais informações, consulte [descritores de segurança absolutos e Self-Relatives](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winnt. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso de baixo nível](low-level-access-control.md)
</dt> <dt>

[Estruturas de controle de acesso básicas](authorization-structures.md)
</dt> <dt>

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 

