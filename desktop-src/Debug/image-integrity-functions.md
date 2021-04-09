---
description: As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funções de integridade da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010170"
---
# <a name="image-integrity-functions"></a>Funções de integridade da imagem

As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem. As rotinas são fornecidas para adicionar, remover e consultar certificados. Há também uma função disponível para obter o fluxo de bytes de um arquivo de imagem necessário para calcular um resumo de mensagens do arquivo de imagem. Isso é necessário para criar certificados de assinatura.

Cada certificado em um arquivo tem um índice que pode ser alterado à medida que os certificados são removidos. Novos certificados serão sempre adicionados "no final" da lista de certificados existentes. Ou seja, eles serão atribuídos a índices maiores que qualquer índice em uso no momento. Em geral, um aplicativo não deve supor que um determinado certificado tenha o mesmo índice que tinha na última vez em que foi referenciado.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



