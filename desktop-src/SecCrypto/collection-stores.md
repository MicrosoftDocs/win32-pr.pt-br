---
description: Como o número de certificados, listas de certificados revogados (CRLs) e lista de certificados confiáveis (CTLs) na coleção de um usuário aumenta, a organização desses certificados se torna um problema.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Repositórios de coleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829409"
---
# <a name="collection-stores"></a>Repositórios de coleta

Como o número de [*certificados*](../secgloss/c-gly.md), [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs) e [*lista de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) na coleção de um usuário aumenta, a organização desses certificados se torna um problema. Uma solução possível é criar repositórios de certificados separados para manter diferentes tipos de certificados. Essa solução cria um novo problema, pois um aplicativo pode precisar pesquisar vários repositórios diferentes para localizar um certificado específico. O uso de repositórios lógicos ou de coleção resolve esse problema.

Um repositório [*lógico*](../secgloss/l-gly.md) e um repositório de certificados de coleção são grupos de repositórios físicos que aparecem para um aplicativo como um único repositório. Todos os repositórios de membros de um repositório lógico ou de coleção podem ser pesquisados ou enumerados com uma única chamada de função para [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) ou [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).

O uso de repositórios lógicos ou de coleção também fornece flexibilidade que é difícil de alcançar com registros em papel. Um certificado em um único repositório físico pode precisar ser um membro de vários grupos lógicos diferentes. Portanto, um repositório físico individual pode ser membro de mais de um repositório lógico ou de coleção, conforme mostrado na ilustração a seguir.

![repositórios de coleta](images/mancert.png)

Esta ilustração apresenta os seguintes conceitos básicos de repositório de certificados lógicos:

-   Um repositório de certificados de coleção tem um ponteiro para o primeiro bloco de ponteiros para esse repositório de coleta.
-   Cada bloco de ponteiro de um repositório de coleção tem um ponteiro para um repositório irmão e um ponteiro para o próximo bloco de ponteiro da coleção.
-   Cada repositório irmão em uma coleção é um repositório de certificados físico simples.
-   Um repositório de certificados simples pode ser um repositório irmão membro em vários repositórios de coleta diferentes.
-   Os certificados adicionados a um repositório de coleta são fisicamente adicionados a um dos armazenamentos irmãos na coleção.
-   Os certificados em um repositório irmão podem ser acessados por qualquer repositório de coleta no qual o repositório irmão é membro.

Os repositórios de coleta são criados em um aplicativo abrindo um repositório de coleta usando [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) e, em seguida, usando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) para adicionar um repositório irmão aberto ao repositório de coleta. Um repositório irmão pode ser excluído de um repositório de coleta chamando [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

 

 
