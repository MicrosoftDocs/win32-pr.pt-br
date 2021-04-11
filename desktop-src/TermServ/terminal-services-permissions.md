---
title: Serviços de Área de Trabalho Remota permissões
description: Você pode usar as permissões fornecidas para Serviços de Área de Trabalho Remota para controlar como os usuários e grupos acessam o servidor.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1358a4360889bc013beefcee4e029f3572c9c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366131"
---
# <a name="remote-desktop-services-permissions"></a>Serviços de Área de Trabalho Remota permissões

Você pode usar as permissões fornecidas para Serviços de Área de Trabalho Remota para controlar como os usuários e grupos acessam o servidor. Para obter uma descrição dos tipos de permissão padrão e informações mais detalhadas sobre Serviços de Área de Trabalho Remota permissões em geral, consulte a documentação que acompanha a ferramenta administrativa de configuração de Serviços de Área de Trabalho Remota. Para obter informações sobre como configurar essas permissões para o Windows Server 2008, consulte [configurar permissões para conexões de serviços de área de trabalho remota](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

A seguir está uma lista das permissões que você pode definir e as tarefas que as permissões permitem.



| Valor                        | Significado                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informações da consulta<br/> | Consultar sessões e servidores para obter informações.<br/>                                                                                                                |
| Definir informações<br/>   | Configurar propriedades de conexão.<br/>                                                                                                                           |
| Controle remoto<br/>    | Exibir ou controlar ativamente a sessão de outro usuário.<br/>                                                                                                           |
| Logon<br/>             | Faça logon em uma sessão no servidor.<br/>                                                                                                                         |
| Verbos<br/>            | Fazer logoff de um usuário de uma sessão. Lembre-se de que o logoff de um usuário sem aviso pode resultar em perda de dados no cliente.<br/>                                  |
| Mensagem<br/>           | Envie uma mensagem para as sessões de outro usuário.<br/>                                                                                                                 |
| Conectar<br/>           | Conecte-se a outra sessão.<br/>                                                                                                                                |
| Desconectar<br/>        | Desconectar uma sessão.<br/>                                                                                                                                      |
| Canais virtuais<br/>  | Use canais virtuais. Lembre-se de que desativar os canais virtuais desabilita alguns recursos de Serviços de Área de Trabalho Remota, como a área de transferência e o redirecionamento de impressora.<br/> |
| Redefinir<br/>             | Encerrar uma sessão. Lembre-se de que a finalização de uma sessão sem aviso pode resultar na perda de dados no cliente.<br/>                                                    |



 

A permissão de logon é necessária para que um usuário faça logon em uma nova sessão de Serviços de Área de Trabalho Remota. Todas as outras Serviços de Área de Trabalho Remota permissões se aplicam ao controle da sessão de Serviços de Área de Trabalho Remota de outro usuário.

Serviços de Área de Trabalho Remota permissões podem ser concedidas ou definidas para usuários individuais ou grupos. Os usuários também podem herdar permissões como resultado de ser um membro do grupo. No entanto, a negação de uma permissão substitui uma permissão herdada. Por exemplo, os membros do grupo Área de Trabalho Remota usuários (RDU) recebem a permissão de consulta por padrão. Se um administrador definir a permissão de consulta como "Deny" para esse usuário, o usuário não poderá consultar a sessão de outro usuário. Depois que um usuário faz logon em uma sessão, o usuário recebe todas as outras permissões de Serviços de Área de Trabalho Remota para sua sessão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços de Área de Trabalho Remota aplicativos de gerenciamento](terminal-services-management-applications.md)
</dt> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 

