---
title: Direitos de acesso e segurança da área de trabalho
description: A segurança permite controlar o acesso a objetos da área de trabalho. Para obter mais informações sobre segurança, consulte Access-Control Modelo.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805a9b5b3db70bf496d467b774dc7c959030b43d6f89d40aabd0336540b7e56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346686"
---
# <a name="desktop-security-and-access-rights"></a>Direitos de acesso e segurança da área de trabalho

A segurança permite controlar o acesso a objetos da área de trabalho. Para obter mais informações sobre segurança, consulte [Modelo de controle de acesso.](/windows/desktop/SecAuthZ/access-control-model)

Você pode especificar um [descritor de segurança para](/windows/desktop/SecAuthZ/security-descriptors) um objeto de área de trabalho ao chamar a função [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) ou [**CreateDesktopEx.**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) Se você especificar NULL, a área de trabalho obtém um descritor de segurança padrão. As ACLs no descritor de segurança padrão para uma área de trabalho vêm de sua estação de janela pai.

Para obter ou definir o descritor de segurança de um objeto de estação de janela, chame as [**funções GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Quando você chama a [**função OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) ou [**OpenInputDesktop,**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.

Os direitos de acesso válidos para objetos da área de trabalho incluem [os direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) e alguns direitos de acesso específicos do objeto. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                       | Significado                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Necessário para excluir o objeto .                                                                                                                                                                                                                                                       |
| READ \_ CONTROL (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o direito de acesso ACCESS \_ SYSTEM \_ SECURITY. Para obter mais informações, consulte [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right). |
| SYNCHRONIZE (0x00100000L)   | Não há suporte para objetos da área de trabalho.                                                                                                                                                                                                                                                   |
| WRITE \_ DAC (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança para o objeto .                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança para o objeto .                                                                                                                                                                                                              |



 

A tabela a seguir lista os direitos de acesso específicos do objeto.



| Direito de acesso                       | Descrição                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ CREATEMENU (0x0004L)      | Necessário para criar um menu na área de trabalho.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Necessário para criar uma janela na área de trabalho.                                                 |
| \_ENUMERAÇÃO DA ÁREA DE TRABALHO (0x0040L)       | Necessário para que a área de trabalho seja enumerada.                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)     | Necessário para estabelecer qualquer um dos ganchos de janela.                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L) | Necessário para executar a reprodução de diário em uma área de trabalho.                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)   | Necessário para executar a gravação de diário em uma área de trabalho.                                         |
| DESKTOP \_ READOBJECTS (0x0001L)     | Necessário para ler objetos na área de trabalho.                                                    |
| DESKTOP \_ SWITCHDESKTOP (0x0100L)   | Necessário para ativar a área de trabalho usando a [**função SwitchDesktop.**](/windows/win32/api/winuser/nf-winuser-switchdesktop) |
| DESKTOP \_ WRITEOBJECTS (0x0080L)    | Necessário para gravar objetos na área de trabalho.                                                   |



 

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um objeto de área de trabalho contido na estação de janela interativa da sessão de logon do usuário.



<table>
<thead>
<tr class="header">
<th>Direito de acesso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

Você pode solicitar o direito de acesso ACCESS SYSTEM SECURITY a um objeto da área de trabalho se quiser ler ou gravar a \_ \_ SACL do objeto. Para obter mais informações, consulte [ACLs (Listas de Controle](/windows/desktop/SecAuthZ/access-control-lists) de Acesso) e [Direito de Acesso SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

 

 