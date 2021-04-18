---
title: Segurança de desktop e direitos de acesso
description: A segurança permite que você controle o acesso a objetos da área de trabalho. Para obter mais informações sobre segurança, consulte modelo de Access-Control.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366336"
---
# <a name="desktop-security-and-access-rights"></a>Segurança de desktop e direitos de acesso

A segurança permite que você controle o acesso a objetos da área de trabalho. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).

Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um objeto de área de trabalho ao chamar a função [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) . Se você especificar NULL, a área de trabalho obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão de uma área de trabalho são provenientes de sua estação de janela pai.

Para obter ou definir o descritor de segurança de um objeto de estação de janela, chame as funções [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando você chama a função [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) ou [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.

Os direitos de acesso válidos para objetos da área de trabalho incluem os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) e alguns direitos de acesso específicos ao objeto. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                       | Significado                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCLUIR (0x00010000L)        | Necessário para excluir o objeto.                                                                                                                                                                                                                                                       |
| \_Controle de leitura (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o direito de acesso de segurança do sistema de acesso \_ \_ . Para obter mais informações, consulte [direitos de acesso à SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| SINCRONIZAR (0x00100000L)   | Sem suporte para objetos da área de trabalho.                                                                                                                                                                                                                                                   |
| GRAVAR \_ DAC (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança do objeto.                                                                                                                                                                                                               |
| Proprietário da gravação \_ (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança do objeto.                                                                                                                                                                                                              |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto.



| Direito de acesso                       | Descrição                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| CreateMenu da área \_ de trabalho (0x0004L)      | Necessário para criar um menu na área de trabalho.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Necessário para criar uma janela na área de trabalho.                                                 |
| \_Enumerar desktops (0x0040L)       | Necessário para que a área de trabalho seja enumerada.                                                  |
| HOOKCONTROL da área \_ de trabalho (0x0008L)     | Necessário para estabelecer qualquer um dos ganchos de janela.                                              |
| JOURNALPLAYBACK da área \_ de trabalho (0x0020L) | Necessário para executar a reprodução do diário em uma área de trabalho.                                          |
| JOURNALRECORD da área \_ de trabalho (0x0010L)   | Necessário para executar a gravação do diário em uma área de trabalho.                                         |
| READOBJECTS da área \_ de trabalho (0x0001L)     | Necessário para ler objetos na área de trabalho.                                                    |
| SWITCHDESKTOP da área \_ de trabalho (0x0100L)   | Necessário para ativar a área de trabalho usando a função [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) . |
| WRITEOBJECTS da área \_ de trabalho (0x0080L)    | Necessário para gravar objetos na área de trabalho.                                                   |



 

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



 

Você pode solicitar o direito de acesso de segurança do sistema de acesso \_ \_ a um objeto de área de trabalho se quiser ler ou gravar a SACL do objeto. Para obter mais informações, consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [direito de acesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 