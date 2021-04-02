---
description: Identifica as informações de segurança relacionadas ao objeto que estão sendo definidas ou consultadas.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164697"
---
# <a name="security_information"></a>informações de segurança \_

O tipo de dados **\_ informações de segurança** identifica as informações de segurança relacionadas ao objeto que estão sendo definidas ou consultadas. Essas informações de segurança incluem:

-   O proprietário de um objeto
-   O grupo primário de um objeto
-   A DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) de um objeto
-   A SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema de um objeto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Comentários

Alguns membros de **\_ informações de segurança** só funcionam com a função [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) . Esses membros não são retornados na estrutura retornada por outras funções de segurança, como [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Cada item de informações de segurança é designado por um sinalizador de bit. Cada sinalizador de bit pode ser um dos valores a seguir. Para obter mais informações, consulte as funções [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) e [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) .



| Valor/direitos necessários para consultar/definir                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_informações de segurança do atributo \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **gravar \_ DAC**<br/>                                                                                     | As propriedades de recurso do objeto que está sendo referenciado. As propriedades de recurso são armazenadas em \_ tipos de ACE de atributo de recurso do sistema \_ \_ na SACL do descritor de segurança.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Este sinalizador de bit não está disponível.<br/> <br/>                 |
| \_informações de segurança de backup \_<br/> Direito necessário para consultar: **\_ controle de leitura** e **\_ \_ segurança do sistema de acesso**<br/> Direito necessário para definir: **gravar \_ DAC** e **gravar \_ proprietário** e **\_ \_ segurança do sistema de acesso**<br/> | Todas as partes do descritor de segurança. Isso é útil para o software de backup e restauração que precisa preservar o descritor de segurança inteiro.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Este sinalizador de bit não está disponível.<br/> <br/>                                                  |
| \_informações de segurança da DACL \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **gravar \_ DAC**<br/>                                                                                          | A DACL do objeto está sendo referenciada.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_informações de segurança do grupo \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **\_ proprietário da gravação** <br/>                                                                                      | O identificador do grupo primário do objeto está sendo referenciado.<br/>                                                                                                                                                                                                                                                                                                    |
| \_informações de segurança do rótulo \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **\_ proprietário da gravação** <br/>                                                                                      | O rótulo de integridade obrigatório está sendo referenciado.<br/> O rótulo de integridade obrigatório é uma ACE na SACL do objeto.<br/> **Windows Server 2003 e Windows XP:** Este sinalizador de bit não está disponível.<br/> <br/>                                                                                                                                    |
| \_informações de segurança do proprietário \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **\_ proprietário da gravação** <br/>                                                                                      | O identificador de proprietário do objeto está sendo referenciado.<br/>                                                                                                                                                                                                                                                                                                            |
| \_informações de \_ segurança da DACL protegida \_<br/> Direito necessário para consultar: não disponível<br/> Direito necessário para definir: **gravar \_ DAC**<br/>                                                                                   | A DACL não pode herdar as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ).<br/>                                                                                                                                                                                                                   |
| \_informações de \_ segurança de SACL protegidas \_<br/> Direito necessário para consultar: não disponível<br/> Direito necessário para definir: **acesso \_ à \_ segurança do sistema**<br/>                                                                     | A SACL não pode herdar ACEs.<br/>                                                                                                                                                                                                                                                                                                                                      |
| \_informações de segurança da SACL \_<br/> Direito necessário para consultar: **\_ \_ segurança do sistema de acesso**<br/> Direito necessário para definir: **acesso \_ à \_ segurança do sistema**<br/>                                                                 | A SACL do objeto está sendo referenciada.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_informações de segurança do escopo \_<br/> Direito necessário para consultar: **\_ controle de leitura**<br/> Direito necessário para definir: **acesso \_ à \_ segurança do sistema**<br/>                                                                           | O identificador da CAP (política de acesso central) aplicável no objeto que está sendo referenciado. Cada identificador de extremidade é armazenado em um \_ tipo de \_ ACE de ID de política com escopo de sistema \_ \_ na SACL do SD.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Este sinalizador de bit não está disponível.<br/> <br/> |
| informações de segurança da DACL desprotegidas \_ \_ \_<br/> Direito necessário para consultar: não disponível<br/> Direito necessário para definir: **gravar \_ DAC**<br/>                                                                                 | A DACL herda ACEs do objeto pai.<br/>                                                                                                                                                                                                                                                                                                                     |
| informações de segurança de SACL desprotegidas \_ \_ \_<br/> Direito necessário para consultar: não disponível<br/> Direito necessário para definir: **acesso \_ à \_ segurança do sistema**<br/>                                                                   | A SACL herda ACEs do objeto pai.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winnt. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso](access-control.md)
</dt> <dt>

[Estruturas de controle de acesso básicas](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

