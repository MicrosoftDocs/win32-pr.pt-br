---
description: O Windows de segurança permite controlar o acesso às chaves do Registro. Para obter mais informações sobre segurança, consulte Access-Control Modelo.
ms.assetid: 266d5c8e-1bcd-48e5-bc06-2fbc956d8658
title: Direitos de acesso e segurança de chave do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0797eeff4923574007c2e1d7751121767c894f91a42316ff5d581ee2d18b6d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885199"
---
# <a name="registry-key-security-and-access-rights"></a>Direitos de acesso e segurança de chave do Registro

O Windows de segurança permite controlar o acesso às chaves do Registro. Para obter mais informações sobre segurança, consulte [Modelo de controle de acesso.](/windows/desktop/SecAuthZ/access-control-model)

Você pode especificar um [descritor de](/windows/desktop/SecAuthZ/security-descriptors) segurança para uma chave do Registro ao chamar a função [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) ou [**RegSetKeySecurity.**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity) Se você especificar **NULL,** a chave obtém um descritor de segurança padrão. As ACLs em um descritor de segurança padrão para uma chave são herdadas de sua chave pai direta.

Para obter o descritor de segurança de uma chave do Registro, chame a função [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity), [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa)ou [**GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo)

Os direitos de acesso válidos para chaves do Registro incluem os direitos de acesso padrão DELETE, READ \_ CONTROL, WRITE DAC e \_ WRITE \_ [](/windows/desktop/SecAuthZ/standard-access-rights)OWNER. As chaves do Registro não são suportadas pelo direito de acesso padrão SYNCHRONIZE.

A tabela a seguir lista os direitos de acesso específicos para objetos de chave do Registro.



| Valor                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KEY \_ ALL \_ ACCESS (0xF003F)<br/>         | Combina os direitos PADRÃO NECESSÁRIOS, O VALOR DA CONSULTA DE CHAVE, O VALOR DO CONJUNTO DE CHAVES, A SUB-CHAVE KEY CREATE, AS SUB KEYS DE ENUMERAÇÃO DE CHAVE, a NOTIFICAÇÃO DE CHAVE e os direitos de acesso DO KEY \_ \_ \_ \_ CREATE \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ LINK.<br/>                                                                                                                                                                                                                                                                           |
| KEY \_ CREATE \_ LINK (0x0020)<br/>         | Reservado para uso do sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| KEY \_ CREATE SUB KEY \_ \_ (0x0004)<br/>     | Necessário para criar uma sub-chave de uma chave do Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_SUB-CHAVES \_ DE \_ ENUMERAÇÃO DE CHAVE (0X0008)<br/> | Necessário para enumerar as sub-chaves de uma chave do Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| KEY \_ EXECUTE (0x20019)<br/>             | Equivalente a KEY \_ READ.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| NOTIFICAÇÃO \_ DE CHAVE (0x0010)<br/>               | Necessário para solicitar notificações de alteração para uma chave do Registro ou para sub-chaves de uma chave do Registro.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| KEY \_ QUERY \_ VALUE (0x0001)<br/>         | Necessário para consultar os valores de uma chave do Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| LEITURA \_ DE CHAVE (0x20019)<br/>                | Combina os valores STANDARD \_ RIGHTS \_ READ, KEY \_ QUERY \_ VALUE, KEY \_ ENUMERATE \_ SUB KEYS e \_ KEY \_ NOTIFY.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| KEY \_ SET \_ VALUE (0x0002)<br/>           | Necessário para criar, excluir ou definir um valor do Registro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| KEY \_ WOW64 \_ 32KEY (0x0200)<br/>         | Indica que um aplicativo em um Windows de 64 bits deve operar na exibição do Registro de 32 bits. Esse sinalizador é ignorado por 32 bits Windows. Para obter mais informações, [consulte Acessando uma exibição de registro alternativa.](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)<br/> Esse sinalizador deve ser combinado usando o operador OR com os outros sinalizadores nesta tabela que consultam ou acessam valores do Registro.<br/> **Windows 2000:** Não há suporte para esse sinalizador.<br/> |
| KEY \_ WOW64 \_ 64KEY (0x0100)<br/>         | Indica que um aplicativo em um Windows de 64 bits deve operar na exibição do Registro de 64 bits. Esse sinalizador é ignorado por 32 bits Windows. Para obter mais informações, [consulte Acessando uma exibição de registro alternativa.](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)<br/> Esse sinalizador deve ser combinado usando o operador OR com os outros sinalizadores nesta tabela que consultam ou acessam valores do Registro.<br/> **Windows 2000:** Não há suporte para esse sinalizador.<br/> |
| GRAVAÇÃO \_ DE CHAVE (0x20006)<br/>               | Combina os direitos de \_ acesso STANDARD RIGHTS \_ WRITE, KEY SET VALUE e \_ KEY CREATE SUB \_ \_ \_ \_ KEY.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

Quando você chama a [**função RegOpenKeyEx,**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) o sistema verifica os direitos de acesso solicitados no descritor de segurança da chave. Se o usuário não tiver o acesso correto à chave do Registro, a operação aberta falhará. Se um administrador precisar acessar a chave, a solução será habilitar o privilégio ES TAKE OWNERSHIP NAME e abrir a chave do Registro com acesso \_ \_ WRITE \_ \_ OWNER. Para obter mais informações, consulte [Habilitando e desabilitando privilégios](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Você pode solicitar o direito de acesso ACCESS SYSTEM SECURITY a uma chave do Registro se quiser ler ou gravar a SACL (lista de controle de acesso do \_ \_ sistema) da chave. Para obter mais informações, consulte [ACLs (Listas de Controle](/windows/desktop/SecAuthZ/access-control-lists) de Acesso) e [Direito de Acesso SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

Para exibir os direitos de acesso atuais de uma chave, incluindo as chaves predefinida, use o Editor do Registro (Regedt32.exe). Depois de navegar até a chave desejada, vá para o menu **Editar** e selecione **Permissões**.

 

