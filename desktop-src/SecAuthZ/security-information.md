---
description: Identifica as informações de segurança relacionadas ao objeto que estão sendo definidas ou consultadas.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eda92db81cc2325dcc2eb084c06aa5ac7ca92475cca92d8221e394af9704c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907196"
---
# <a name="security_information"></a>INFORMAÇÕES DE \_ SEGURANÇA

O **tipo de dados SECURITY \_ INFORMATION** identifica as informações de segurança relacionadas ao objeto que estão sendo definidas ou consultadas. Essas informações de segurança incluem:

-   O proprietário de um objeto
-   O grupo primário de um objeto
-   A [*DACL (lista de controle de*](/windows/desktop/SecGloss/d-gly) acesso discricionário) de um objeto
-   A [*SACL*](/windows/desktop/SecGloss/s-gly) (lista de controle de acesso do sistema) de um objeto


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Comentários

Alguns **membros de INFORMAÇÕES \_ DE** SEGURANÇA funcionam apenas com a [**função SetNamedSecurityInfo.**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) Esses membros não são retornados na estrutura retornada por outras funções de segurança, como [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Cada item de informações de segurança é designado por um sinalizador de bit. Cada sinalizador de bit pode ser um dos valores a seguir. Para obter mais informações, consulte as funções [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) e [**QuerySecurityAccessMask.**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)



| Valor/direitos necessários para consultar/definir                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INFORMAÇÕES \_ DE SEGURANÇA DE \_ ATRIBUTO<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **WRITE \_ DAC**<br/>                                                                                     | As propriedades de recurso do objeto que está sendo referenciado. As propriedades do recurso são armazenadas em tipos \_ ACE DE ATRIBUTO DE RECURSO DO SISTEMA na \_ \_ SACL do descritor de segurança.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Esse sinalizador de bit não está disponível.<br/> <br/>                 |
| INFORMAÇÕES \_ DE SEGURANÇA DE \_ BACKUP<br/> Direito necessário para consultar: **READ \_ CONTROL e** ACCESS SYSTEM **\_ \_ SECURITY**<br/> Direito necessário para definir: **GRAVAR \_ DAC** e **GRAVAR PROPRIETÁRIO e \_ ACESSAR** **SEGURANÇA DO \_ \_ SISTEMA**<br/> | Todas as partes do descritor de segurança. Isso é útil para backup e restauração de software que precisa preservar todo o descritor de segurança.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Esse sinalizador de bit não está disponível.<br/> <br/>                                                  |
| INFORMAÇÕES DE SEGURANÇA \_ DACL \_<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **WRITE \_ DAC**<br/>                                                                                          | A DACL do objeto está sendo referenciada.<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMAÇÕES \_ DE SEGURANÇA DE \_ GRUPO<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **GRAVAR \_ PROPRIETÁRIO** <br/>                                                                                      | O identificador de grupo primário do objeto está sendo referenciado.<br/>                                                                                                                                                                                                                                                                                                    |
| INFORMAÇÕES DE \_ SEGURANÇA DO \_ RÓTULO<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **GRAVAR \_ PROPRIETÁRIO** <br/>                                                                                      | O rótulo de integridade obrigatório está sendo referenciado.<br/> O rótulo de integridade obrigatório é uma ACE na SACL do objeto .<br/> **Windows Server 2003 e Windows XP:** Esse sinalizador de bit não está disponível.<br/> <br/>                                                                                                                                    |
| INFORMAÇÕES DE \_ SEGURANÇA \_ DO PROPRIETÁRIO<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **GRAVAR \_ PROPRIETÁRIO** <br/>                                                                                      | O identificador de proprietário do objeto está sendo referenciado.<br/>                                                                                                                                                                                                                                                                                                            |
| INFORMAÇÕES DE \_ SEGURANÇA DACL \_ \_ PROTEGIDAS<br/> Direito necessário para consultar: Não disponível<br/> Direito necessário para definir: **WRITE \_ DAC**<br/>                                                                                   | A DACL não pode herdar [*ACEs*](/windows/desktop/SecGloss/a-gly) (entradas de controle de acesso).<br/>                                                                                                                                                                                                                   |
| INFORMAÇÕES DE \_ SEGURANÇA SACL \_ \_ PROTEGIDAS<br/> Direito necessário para consultar: Não disponível<br/> Direito necessário para definir: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                     | O SACL não pode herdar ACEs.<br/>                                                                                                                                                                                                                                                                                                                                      |
| INFORMAÇÕES DE \_ SEGURANÇA \_ SACL<br/> Direito necessário para consultar: **ACCESS \_ SYSTEM \_ SECURITY**<br/> Direito necessário para definir: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                 | A SACL do objeto está sendo referenciada.<br/>                                                                                                                                                                                                                                                                                                                        |
| INFORMAÇÕES DE \_ SEGURANÇA DE \_ ESCOPO<br/> Direito necessário para consultar: **READ \_ CONTROL**<br/> Direito necessário para definir: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                           | O identificador CAP (Política de Acesso Central) aplicável ao objeto que está sendo referenciado. Cada identificador CAP é armazenado em um tipo ACE de ID DE POLÍTICA DE ESCOPO DO SISTEMA \_ \_ na \_ \_ SACL do SD.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Esse sinalizador de bit não está disponível.<br/> <br/> |
| INFORMAÇÕES DE \_ SEGURANÇA DACL DESPROTEGIDAS \_ \_<br/> Direito necessário para consultar: Não disponível<br/> Direito necessário para definir: **WRITE \_ DAC**<br/>                                                                                 | A DACL herda ACEs do objeto pai.<br/>                                                                                                                                                                                                                                                                                                                     |
| INFORMAÇÕES DE \_ SEGURANÇA SACL DESPROTEGIDAS \_ \_<br/> Direito necessário para consultar: Não disponível<br/> Direito necessário para definir: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                   | A SACL herda ACEs do objeto pai.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso](access-control.md)
</dt> <dt>

[Estruturas básicas de controle de acesso](authorization-structures.md)
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

 

