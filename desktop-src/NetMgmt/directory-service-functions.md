---
title: Funções de serviço de diretório (gerenciamento de rede)
description: As funções de serviço de diretório de gerenciamento de rede permitem que os desenvolvedores trabalhem com o controlador de domínio e a associação de domínio no serviço de diretório.
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e843e06762b4a7ef55b3f979b12a62ee6adf3
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104008584"
---
# <a name="directory-service-functions"></a>Funções de serviço de diretório

As funções de serviço de diretório de gerenciamento de rede permitem que os desenvolvedores trabalhem com o controlador de domínio e a associação de domínio no serviço de diretório.

As funções de serviço de diretório de gerenciamento de rede são listadas a seguir.



| Função                                                                 | Descrição                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | Adiciona um nome alternativo para o computador especificado.                                                                                                                                          |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | Enumera nomes para o computador especificado.                                                                                                                                                |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | Recupera uma lista de UOs (unidades organizacionais) nas quais uma conta de computador pode ser criada.                                                                                                  |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | Recupera informações de status de junção para o computador especificado.                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | Une um computador a um grupo de trabalho ou domínio.                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | Provisiona uma conta de computador para uso posterior em uma operação de ingresso no domínio offline.                                                                                                           |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | Remove um nome alternativo para o computador especificado.                                                                                                                                       |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | Altera o nome de um computador em um domínio.                                                                                                                                                 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | Define o nome do computador primário para o computador especificado.                                                                                                                                  |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Desassocia um computador de um grupo de trabalho ou domínio.                                                                                                                                            |
| [**Netvalidaname**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | Verifica a validade de um nome de computador, nome de grupo de trabalho ou nome de domínio.                                                                                                                   |



 

Para obter mais informações sobre programação para Active Directory, consulte a [referência de Active Directory](/windows/desktop/AD/active-directory-domain-services-reference). Para obter mais informações sobre unidades organizacionais, consulte [Managing Users](/windows/desktop/AD/managing-users) in the Active Directory Documentation.

 

 