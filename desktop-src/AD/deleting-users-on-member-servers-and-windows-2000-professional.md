---
title: excluindo usuários em servidores membros e Windows 2000 Professional
description: este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- usuários AD, excluindo um usuário em servidores membros e Windows 2000 Professional
- Active Directory, usando, usuários, excluindo usuários em servidores membros e Windows 2000 Professional
- excluindo um usuário
- servidor, excluindo um usuário
- excluindo usuários em servidores membros e Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e366356696c1e8b11a53b45aae3860600fc6555
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881455"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>excluindo usuários em servidores membros e Windows 2000 Professional

este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.

**Para excluir um usuário**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para informar ao ADSI que ele está ligando a um computador: "WinNT:// <computer name> , &lt; Computer &gt; ". O &lt; parâmetro "nome &gt; do computador" é o nome do computador cujos grupos você deseja acessar. Esse parâmetro notifica a ADSI que ele está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.
    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "user" como a classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para excluir o usuário.

    Lembre-se de que você não precisa chamar [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar a alteração no contêiner. A chamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma a exclusão do usuário diretamente no diretório.

 

 
