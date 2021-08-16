---
title: enumerando usuários em servidores membros e Windows 2000 Professional
description: este tópico mostra como enumerar todos os usuários, em um banco de dados de segurança local, em servidores membros e computadores em execução no Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- enumerando usuários em servidores membros e Windows 2000 Professional AD
- o AD dos usuários, enumerando usuários em servidores membros e Windows 2000 Professional
- Active Directory, usando, usuários, enumerando usuários em servidores membros e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694873"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>enumerando usuários em servidores membros e Windows 2000 Professional

este tópico mostra como enumerar todos os usuários, em um banco de dados de segurança local, em servidores membros e computadores em execução no Windows 2000 Professional.

**Para enumerar os usuários**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta que tenha direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para instruir a ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ". O &lt; parâmetro "nome &gt; do computador" é o nome do computador para cujos grupos serão acessados. Esse parâmetro instrui a ADSI de que ela está vinculando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar o tipo de objeto ao qual você está ligando.
    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Adicione "user" à propriedade [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) . Isso faz com que a enumeração contenha apenas objetos que tenham a classe de objeto "user".
3.  Enumere os objetos. Para cada objeto de usuário, use os métodos de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) para ler as propriedades do usuário.

 

 