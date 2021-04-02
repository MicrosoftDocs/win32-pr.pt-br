---
description: O futuro da criptografia e das comunicações seguras não podem ser facilmente previstos.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Estendendo a funcionalidade de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922681"
---
# <a name="extending-cryptoapi-functionality"></a>Estendendo a funcionalidade de CryptoAPI

O futuro da [*criptografia*](../secgloss/c-gly.md) e das comunicações seguras não podem ser facilmente previstos. Novos tipos de certificado podem surgir, várias extensões de certificado podem encontrar uso comum e novos tipos de mensagem podem ser introduzidos. Por isso, a extensibilidade faz parte do design das principais funções de [*CryptoAPI*](../secgloss/c-gly.md) .

As seções a seguir apresentam visões gerais sobre o uso de OIDs para estender funções de CryptoAPI.



| Tópico                                                                              | Sumário                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral de OID](oid-overview.md)                                                   | Conceitos básicos de OID.                                                                                                           |
| [Criando a nova funcionalidade](creating-the-new-functionality.md)               | Criando OIDs e funções para estender o uso de APIs existentes.                                                                     |
| [Registrando a nova funcionalidade](registering-the-new-functionality.md)         | Configurando novas funções relacionadas a OID.                                                                                               |
| [Instalando a nova funcionalidade](installing-the-new-functionality.md)           | Instalando funções de OID na memória para melhorar o desempenho.                                                                          |
| [Estendendo a funcionalidade CertOpenStore](extending-certopenstore-functionality.md) | Estendendo a funcionalidade [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) usando a função instalável ou registrada do provedor de repositório de certificados. |



 

 

 
