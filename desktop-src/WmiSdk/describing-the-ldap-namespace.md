---
description: Ao conectar-se remotamente a um servidor Active Directory diferente daquele em seu domínio atual, você deve especificar o nome de um computador que já seja membro do domínio pertencente ao Active Directory desejado.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descrevendo o namespace LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad19ea98e5bd6f36ff78159bfe0a106f0772921c152aa167c38e435732188446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568616"
---
# <a name="describing-the-ldap-namespace"></a>Descrevendo o namespace LDAP

Ao conectar-se remotamente a um servidor Active Directory diferente daquele em seu domínio atual, você deve especificar o nome de um computador que já seja membro do domínio pertencente ao Active Directory desejado.

Para se conectar remotamente a um computador que já é membro do domínio pertencente ao servidor de Active Directory, digite o comando a seguir.

**\\\\\\ \\ LDAP do diretório raiz do computador_remoto \\**

Este exemplo mostra que há duas partes que compõem um nome de namespace totalmente qualificado. A primeira parte ( \\ \\ computador_remoto) representa o computador que já é membro do domínio pertencente ao servidor de Active Directory que você deseja. A segunda parte ( \\ \\ LDAP do diretório raiz \\ ) representa o esquema de Active Directory no provedor de serviços de diretório.

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



