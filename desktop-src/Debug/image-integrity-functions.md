---
description: As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funções de integridade da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957095"
---
# <a name="image-integrity-functions"></a>Funções de integridade da imagem

As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem. Rotinas são fornecidas para adicionar, remover e consultar certificados. Também há uma função disponível para obter o fluxo de byte de um arquivo de imagem necessário para calcular um resumo de mensagem do arquivo de imagem. Isso é necessário para criar certificados de assinatura.

Cada certificado em um arquivo tem um índice que pode ser alterado à medida que os certificados são removidos. Novos certificados sempre serão adicionados "no final" da lista de certificados existentes. Ou seja, eles receberão índices maiores do que qualquer índice em uso no momento. Em geral, um aplicativo não deve assumir que um determinado certificado tem o mesmo índice que tinha na última vez em que foi referenciado.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



