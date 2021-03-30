---
title: Problemas de autenticação para ADSI com ASP
description: Dependendo da configuração da sua intranet, podem ocorrer problemas de autenticação quando o código ADSI é executado em uma página ASP.
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI, páginas ASP, problemas de autenticação
- Problemas de ADSI, autenticação e ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641825"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>Problemas de autenticação para ADSI com ASP

Dependendo da configuração da sua intranet, podem ocorrer problemas de autenticação quando o código ADSI é executado em uma página ASP.

A autenticação para acessar o controlador de domínio pode ser fornecida usando a delegação. A delegação permite que um serviço atue como o usuário, para que ele possa acessar um recurso de rede usando essas credenciais de usuário. Se a sua intranet seguir essa configuração, você deverá configurar o IIS para usar a delegação. Defina o mecanismo de autenticação do IIS como anônimo ou NTLM. Se você escolher anônimo, seu contexto de segurança será mapeado para a \_ conta da máquina IUSR. Se você selecionar NTLM, o contexto de segurança será alterado, dependendo de qual usuário fizer logon no seu site. Para obter mais informações e instruções sobre como configurar o servidor IIS para delegação, consulte [Windows 2000 Resource Kit](https://support.microsoft.com/kb/927229).

Se você estiver usando um servidor IIS que usa o desafio/resposta NT ou um cliente de navegador que não oferece suporte a Kerberos, a autenticação de salto duplo não terá suporte. Autenticação de salto duplo significa que as credenciais do usuário são passadas do cliente de navegador para o servidor IIS e, em seguida, o servidor IIS passa as credenciais para o servidor de back-end. Nessa situação, você pode usar uma das seguintes soluções para permitir o acesso ao diretório na página ASP:

-   Use [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) para passar credenciais para Active Directory. A página da Web autentica o usuário conectado no servidor IIS. Quando o usuário foi autenticado, a página da Web pode usar OpenDSObject ou ADsOpenObject para passar um nome de usuário e senha para o serviço de diretório para obter a autenticação para o servidor de back-end. A página da Web pode então acessar dados do diretório.
-   Adicione seu código a um objeto COM e coloque esse objeto em um [aplicativo com+](../cossdk/com--application-overview.md) (anteriormente chamado de pacote MTS). O aplicativo COM+ pode ser executado como uma [conta de usuário de domínio](/windows/desktop/AD/domain-user-accounts).
-   Use várias páginas ASP, em que uma página autentica o cliente e uma outra página passa credenciais para o diretório usando a autenticação anônima em uma conta de usuário de domínio.

Esses métodos envolvem a autenticação do cliente Web e a alteração das credenciais ao entrar em contato com o diretório porque a autenticação de salto duplo, com as mesmas credenciais, não é possível.

 

 