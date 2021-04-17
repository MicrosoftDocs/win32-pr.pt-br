---
title: Segurança de estação de janela e direitos de acesso
description: A segurança permite que você controle o acesso a objetos de estação de janela. Para obter mais informações sobre segurança, consulte modelo de Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790255"
---
# <a name="window-station-security-and-access-rights"></a>Segurança de estação de janela e direitos de acesso

A segurança permite que você controle o acesso a objetos de estação de janela. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).

Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um objeto de estação de janela ao chamar a função [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) . Se você especificar NULL, a estação de janela obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão para uma estação de janela são provenientes do token principal ou de representação do criador.

Para obter ou definir o descritor de segurança de um objeto de estação de janela, chame as funções [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando você chama a função [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.

Os direitos de acesso válidos para objetos de estação de janela incluem os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) e alguns direitos de acesso específicos ao objeto. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                       | Significado                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXCLUIR (0x00010000L)        | Necessário para excluir o objeto.                                                                                                                                                                                                                                                       |
| \_Controle de leitura (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o direito de acesso de segurança do sistema de acesso \_ \_ . Para obter mais informações, consulte [direitos de acesso à SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| SINCRONIZAR (0x00100000L)   | Sem suporte para objetos de estação de janela.                                                                                                                                                                                                                                            |
| GRAVAR \_ DAC (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança do objeto.                                                                                                                                                                                                               |
| Proprietário da gravação \_ (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança do objeto.                                                                                                                                                                                                              |



 

A tabela a seguir lista os direitos de acesso específicos ao objeto.



| Direito de acesso                        | Descrição                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ todo o \_ acesso (0x37F)         | Todos os direitos de acesso possíveis para a estação de janela.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Necessário para usar a área de transferência.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Necessário para manipular Atoms globais.                                                                                                                                                                                                                                          |
| WINSTA \_ createdesktop (0x0008L)     | Necessário para criar novos objetos da área de trabalho na estação de janela.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Necessário para enumerar objetos da área de trabalho existentes.                                                                                                                                                                                                                               |
| WINSTA \_ enumerar (0x0100L)         | Necessário para que a estação de janela seja enumerada.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Necessário para chamar com êxito a função [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) . As estações de janela podem ser compartilhadas por usuários e esse tipo de acesso pode impedir que outros usuários de uma estação de janela façam logoff do proprietário da estação de janela. |
| WINSTA \_ ReadAttributes (0x0002L)    | Necessário para ler os atributos de um objeto de estação de janela. Esse atributo inclui configurações de cores e outras propriedades de estação de janela global.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Necessário para acessar o conteúdo da tela.                                                                                                                                                                                                                                           |
| WINSTA \_ WriteAttributes (0x0010L)   | Necessário para modificar os atributos de um objeto de estação de janela. Os atributos incluem configurações de cor e outras propriedades de estação de janela global.                                                                                                                               |



 

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para o objeto de estação de janela interativa, que é a estação de janela atribuída à sessão de logon do usuário interativo.



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um objeto de estação de janela não interativa. O sistema atribui estações de janela não interativas a todas as sessões de logon que não sejam do usuário interativo.



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Você pode solicitar o direito de acesso de segurança do sistema de acesso \_ \_ a um objeto de estação de janela se desejar ler ou gravar a SACL do objeto. Para obter mais informações, consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [direito de acesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 