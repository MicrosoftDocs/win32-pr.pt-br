---
title: Criando usuários em servidores membros e no Windows 2000 Professional
description: Este tópico descreve as etapas usadas para criar um usuário em um servidor membro ou computador que executa o Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Criando usuários em servidores membros e no AD do Windows 2000 Professional
- AD de usuários, criando um usuário em servidores membros e no Windows 2000 Professional
- Active Directory, usando, usuários, criando um usuário em servidores membros e no Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007336"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Criando usuários em servidores membros e no Windows 2000 Professional

**Para criar um usuário**

1.  Associe-se ao computador usando as seguintes regras:
    1.  Use uma conta que tenha direitos suficientes para acessar esse computador.
    2.  Use o seguinte formato de cadeia de vinculação usando o provedor WinNT, o nome do computador e um parâmetro extra para informar ao ADSI que ele está ligando a um computador: "WinNT:// <computer name> <computer> ". O &lt; computador "nome &gt; do computador" é o nome do computador cujos grupos você deseja acessar. Esse parâmetro informa ao ADSI que ele está associando a um computador e permite que o analisador do provedor WinNT ignore algumas consultas de resolução de ambigüidade para determinar o tipo de objeto ao qual você está ligando.
    3.  Associe-se à interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "user" como a classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para adicionar o usuário.
3.  Grave o usuário no banco de dados de segurança do computador usando [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 