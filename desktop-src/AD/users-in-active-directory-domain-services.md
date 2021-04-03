---
title: Usuários no Active Directory Domain Services
description: O Active Directory Domain Services inclui um serviço de diretório que armazena dados de domínio, usuário, grupo de usuários e segurança.
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Usuários no Active Directory Domain Services Active Directory
- usuários, serviços de domínio do Active Directory
- serviços de domínio Active Directory, usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007283"
---
# <a name="users-in-active-directory-domain-services"></a>Usuários no Active Directory Domain Services

O Active Directory Domain Services inclui um serviço de diretório que armazena dados de domínio, usuário, grupo de usuários e segurança.

No Windows NT 4,0 e versões anteriores, você pode usar funções como [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel)e assim por diante para gerenciar usuários, grupos de usuários e outros itens de rede. No Windows 2000 e versões posteriores do Windows, a ADSI fornece acesso uniforme e seguro a esses itens e suas propriedades. Lembre-se de que a ADSI fornece um provedor do Windows NT 4,0 que permite usar o ADSI para gerenciar usuários, grupos de usuários e computadores em sistemas Windows NT 4,0. Também há provedores para o Windows Server 2008 Enterprise (instalação do Server Core), o Microsoft Exchange 5,5, o IIS (Microsoft Internet Information Server), o Novell Serviços de diretório do NetWare (NDS) e o Novell NetWare 3. Ou seja, um único conjunto de métodos padronizados para o gerenciamento de usuários e de grupos de usuários para Windows NT, NDS e NetWare 3.

Além disso, o Windows 2000 é um diretório de vários mestres. Ou seja, as alterações para usuários, grupos de usuários e outros dados armazenados no diretório podem ser feitas em qualquer controlador de domínio. No Windows 2000, não é necessário localizar o controlador de domínio primário (PDC) e fazer alterações de usuário e grupo de usuários no PDC.

O Windows 2000 também apresenta um novo namespace hierárquico em um domínio chamado unidade organizacional (UO). Uma UO pode conter computadores, usuários, grupos de usuários e outros objetos de rede. Normalmente, uma UO é usada com a finalidade de agrupar coisas para fins administrativos, como a delegação de direitos administrativos e a atribuição de políticas ao grupo como uma única unidade.

Domínios, UOs, usuários, grupos de usuários, computadores e outros itens de rede são armazenados como objetos no Active Directory Domain Services. No Windows 2000 e versões posteriores do Windows, você ainda adiciona usuários, grupos de usuários e computadores a um domínio. No entanto, agora você tem a opção de adicionar esses objetos a um contêiner de UO ou qualquer outro tipo de contêiner que o objeto que você deseja adicionar define em seu atributo **possSuperior** do objeto **classSchema** ; Esse é um atributo no objeto **classSchema** de um objeto e esse atributo restringe os tipos de objetos que podem conter esse objeto.

 

 