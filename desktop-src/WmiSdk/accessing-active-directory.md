---
description: Active Directory é o serviço de diretório do Windows e é a base das redes distribuídas do Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Acessando Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171457"
---
# <a name="accessing-active-directory"></a>Acessando Active Directory

Active Directory é o serviço de diretório do Windows e é a base das redes distribuídas do Windows. Você pode usar Active Directory para localizar objetos em um domínio de rede de computador, como usuários, políticas de segurança, impressoras, componentes distribuídos e outros recursos. O nome Active Directory se refere ao serviço de diretório e ao próprio diretório.

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

O Windows torna Active Directory acessível por meio do WMI criando um conjunto de referências a cada classe e objeto contidos no Active Directory. Ao acessar o provedor de serviços de diretório por meio do WMI, você pode criar aplicativos habilitados para WMI que podem acessar a riqueza de informações contidas no Active Directory.

Com essas interfaces, você pode:

-   Recupere classes e instâncias.
-   Enumere classes e instâncias.
-   Crie novas instâncias.
-   Modifique as instâncias existentes.
-   Excluir instâncias existentes.
-   Active Directory de consulta.

Os tópicos a seguir podem ajudá-lo a usar o Active Directory com o WMI:

-   [Usando a sintaxe de Active Directory apropriada](using-the-proper-active-directory-syntax.md)
-   [Mapeando Active Directory para o WMI](mapping-active-directory-to-wmi.md)

 

 



