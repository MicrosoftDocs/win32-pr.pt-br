---
description: O CryptoAPI fornece funções para trabalhar com certificados, listas de certificados revogados (CRLs) e listas de certificados confiáveis (CTLs).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Operações com certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829528"
---
# <a name="operations-with-certificates"></a>Operações com certificados

O [*CryptoAPI*](../secgloss/c-gly.md) fornece funções para trabalhar com [*certificados*](../secgloss/c-gly.md), [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs) e listas de [*certificados confiáveis*](../secgloss/c-gly.md) (CTLs). Isso inclui funções para converter tipos codificados em tipos de contexto, funções que duplicam objetos e funções que liberam esses objetos. Essas funções codificam informações em contextos, mas não adicionam esse contexto a nenhuma loja. Essas funções são [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)e [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Use a função CertFree apropriada para liberar contextos criados por uma dessas funções.

As funções de CryptoAPI para duplicar certificados, CRLs e CTLs incrementam o [*contador de referência*](../secgloss/r-gly.md) no contexto especificado e retornam um ponteiro para o contexto. As funções de duplicação não alocam espaço adicional nem copiam os dados de um contexto para um novo local da memória. Essas funções são [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)e [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). Contextos criados com qualquer uma dessas funções devem ser liberados usando a função CertFree apropriada.

As funções de CryptoAPI que liberam certificados, CRLs e CTLs são [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Cada uma dessas funções diminui a [*contagem de referência*](../secgloss/r-gly.md) em um contexto. Se a contagem de referência chegar a zero, a memória alocada para o contexto será liberada.

Para obter listas completas de funções para trabalhar com certificados, CRLs e CTLs, consulte [funções de manutenção do repositório de certificados e certificado](cryptography-functions.md), [funções de certificado](cryptography-functions.md), [funções da lista de certificados revogados](cryptography-functions.md)e [funções de lista de certificados confiáveis](cryptography-functions.md).

 

 
