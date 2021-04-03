---
title: Excluindo usuários em servidores membros e no Windows 2000 Professional
description: Este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.
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
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007328"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Excluindo usuários em servidores membros e no Windows 2000 Professional

Este tópico mostra como excluir um usuário de um servidor membro ou computador que executa o Windows 2000 Professional.

**Para excluir um usuário**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta com direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para informar ao ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ". O &lt; parâmetro "nome &gt; do computador" é o nome do computador cujos grupos você deseja acessar. Esse parâmetro notifica a ADSI que ele está ligando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar a qual tipo de objeto você está ligando.
    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "user" como a classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) para excluir o usuário.

    Lembre-se de que você não precisa chamar [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar a alteração no contêiner. A chamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma a exclusão do usuário diretamente no diretório.

 

 