---
title: Grupos em servidores membros e Windows 2000 Professional
description: Em servidores membros e computadores em execução Windows 2000 Professional, há um banco de dados de segurança local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos em servidores membros e Windows 2000 Professional AD
- grupos do AD , grupos em servidores membros e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e376faf96621018867e46ac021e4aeab6e7fef6cd4e304d26902cb15a4d081f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692913"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Grupos em servidores membros e Windows 2000 Professional

Em servidores membros e computadores em execução Windows 2000 Professional, há um banco de dados de segurança local. Esse banco de dados de segurança local pode conter seus próprios usuários locais e grupos locais cujo escopo é apenas o computador específico em que eles são criados. Ao gerenciar esses tipos de usuários e grupos em servidores membros e computadores em execução no Windows NT Workstation ou Windows 2000 Professional, use o provedor WinNT.

Quando um servidor membro ou um computador em execução no Windows 2000 Professional ou Windows 2000 Professional for membro de um domínio do Windows 2000, os grupos ou usuários no domínio poderão ser usados no banco de dados de segurança local para conceder direitos a esse grupo nesse computador específico.

Ao gerenciar grupos em um Windows 2000 usando ADSI, use o provedor LDAP. Ao gerenciar grupos em servidores membros e computadores em execução no Windows NT Workstation ou Windows 2000 Professional, use o provedor WinNT.

Você deve vincular, pelo menos uma instância, a cada provedor: 1) Vincular ao provedor LDAP para recuperar o ADsPath ao grupo ou usuário que você deseja adicionar a um grupo no banco de dados local e 2) A vincular ao provedor WinNT para adicionar esse usuário ou grupo a um grupo local.

 

 




