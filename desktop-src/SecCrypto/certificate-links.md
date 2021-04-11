---
description: As funções CertAddCertificateLinkToStore, CertAddCRLLinkToStore e CertAddCTLLinkToStore adicionam links a contextos existentes em repositórios de certificados em vez de adicionar cópias desses contextos.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Links de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091519"
---
# <a name="certificate-links"></a>Links de certificado

As funções [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)e [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) adicionam links a contextos existentes em [*repositórios de certificados*](../secgloss/c-gly.md) em vez de adicionar cópias desses contextos. A adição de links a lojas torna o mesmo [*certificado*](../secgloss/c-gly.md)físico, [*CRL*](../secgloss/c-gly.md)ou [*CTL*](../secgloss/c-gly.md) disponível por meio de vários repositórios diferentes. As alterações feitas nas propriedades estendidas de um [*contexto*](../secgloss/c-gly.md) do repositório do contexto original ou de uma loja em que um link para esse contexto são armazenadas, estão disponíveis na loja que contém o contexto original e em todos os outros repositórios que têm links para esse contexto.

Para obter um exemplo que usa [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), consulte [exemplo C programa: operações de repositório de certificados](example-c-program-certificate-store-operations.md).

![links de certificado](images/mancert1.png)

Suponha que os certificados A. 1, A. 2, A. 3 e A. 4 estejam originalmente no armazenamento A e os certificados B. 1, B. 2, B. 3 e B. 4 estão originalmente no repositório B.

-   O diagrama mostra um link adicionado no repositório B para o certificado A. 2 e um link adicionado no repositório A para o certificado B. 2.
-   O original do certificado A. 2 ainda está no armazenamento A. O original de B. 2 ainda está no armazenamento B.
-   Todas as alterações feitas nas propriedades estendidas do certificado A. 2 ou do certificado B. 2 do armazenamento A ou da loja B estarão disponíveis para ambos os repositórios.
-   Se uma cópia do certificado A. 3 tiver sido feita e armazenada no repositório B, quaisquer alterações nas propriedades estendidas do certificado original A. 3 feito do repositório A não ficarão visíveis na nova cópia no repositório B. Se foram feitas alterações nas propriedades estendidas da cópia do certificado A. 3 no repositório B, essas alterações não afetariam o conteúdo do certificado original A. 3 e não seriam visíveis no armazenamento A.

 

 
