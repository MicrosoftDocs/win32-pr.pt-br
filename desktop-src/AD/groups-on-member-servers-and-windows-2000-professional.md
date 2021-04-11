---
title: Grupos em servidores membros e no Windows 2000 Professional
description: Em servidores membros e computadores em execução no Windows 2000 Professional, há um banco de dados de segurança local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos em servidores membros e AD do Windows 2000 Professional
- grupos de anúncios, grupos em servidores membros e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291810"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Grupos em servidores membros e no Windows 2000 Professional

Em servidores membros e computadores em execução no Windows 2000 Professional, há um banco de dados de segurança local. Esse banco de dados de segurança local pode conter seu próprio usuário local e grupos locais cujo escopo é apenas o computador em que eles são criados. Ao gerenciar esses tipos de usuários e grupos em servidores membros e computadores em execução no Windows NT Workstation ou no Windows 2000 Professional, use o provedor WinNT.

Quando um servidor membro ou um computador que executa o Windows 2000 Professional ou o Windows 2000 Professional é membro de um domínio do Windows 2000, os grupos ou usuários no domínio podem ser usados no banco de dados de segurança local para conceder direitos a esse grupo nesse computador específico.

Ao gerenciar grupos em um domínio do Windows 2000 usando ADSI, use o provedor LDAP. Ao gerenciar grupos em servidores membros e computadores em execução no Windows NT Workstation ou no Windows 2000 Professional, use o provedor WinNT.

Você deve associar, pelo menos uma instância, a cada provedor: 1) associar ao provedor LDAP para recuperar o ADsPath para o grupo ou usuário que você deseja adicionar a um grupo no banco de dados local e 2) associar ao provedor WinNT para adicionar esse usuário ou grupo a um grupo local.

 

 




