---
description: Este tópico lista considerações sobre como usar a API de Assinatura Digital XPS para adicionar assinaturas digitais a um documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso da API de assinatura digital do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469348"
---
# <a name="using-xps-digital-signature-api"></a>Uso da API de assinatura digital do XPS

Este tópico lista considerações sobre como usar a API de Assinatura Digital XPS para adicionar assinaturas digitais a um documento XPS.

A API de Assinatura Digital XPS permite que os aplicativos solicitem que os usuários assinem documentos XPS e verifiquem as assinaturas encontradas em documentos XPS. A API de Assinatura Digital XPS pode ser aplicada a um documento XPS sem carregá-lo em um OM XPS e pode ser usada em fluxos de documentos XPS serializados de um OM XPS.

A seção Tarefas de Programação da API de [Assinatura Digital XPS](#xps-digital-signature-api-programming-tasks) contém tópicos que descrevem como programar com a API de Assinatura Digital XPS. Este tópico lista as considerações a seguir para usar a API de Assinatura Digital XPS ao adicionar suporte de assinatura digital a um aplicativo.

-   [Tarefas de programação da API de Assinatura Digital xps](#xps-digital-signature-api-programming-tasks)
-   [Notas especiais sobre a programação da API de Assinatura Digital xps](#special-notes-about-xps-digital-signature-api-programming)
    -   [Verificando assinaturas digitais em um documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Política de Assinatura Digital](#digital-signature-signing-policy)
    -   [Incorporação de uma cadeia de certificados](#embedding-a-certificate-chain)
    -   [Usando a estrutura CERT \_ CONTEXT](#using-the-cert\_context-structure)
-   [Tópicos relacionados](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Tarefas de programação da API de Assinatura Digital xps

Esta seção contém tópicos que descrevem como executar tarefas de programação usando a API de Assinatura Digital XPS.

-   [Tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md)<dl>

[Inicializar o Gerenciador de Assinaturas](initialize-the-signature-manager.md)  
    [Assinar um documento](sign-a-document.md)  
    [Adicionar uma solicitação de assinatura a um documento XPS](add-a-signature-request-to-a-document.md)  
    [Verificar assinaturas de documento](verify-document-signatures.md)  
    </dl>
-   [Tarefas adicionais de programação de assinatura digital](advanced-digital-signature-programming-tasks.md)<dl>

[Carregar um certificado de um arquivo](load-a-certificate-from-a-file.md)  
    [Verificar se um certificado dá suporte a um método de assinatura](verify-a-certificate-supports-a-signature-method.md)  
    [Verificar se o sistema dá suporte a um método Digest](verify-a-certificate-supports-a-digest-method.md)  
    [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Notas especiais sobre a programação da API de Assinatura Digital xps

Os tópicos a seguir exigem alguma consideração especial ao usar a API de Assinatura Digital XPS.

-   [Verificando assinaturas digitais em um documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Política de Assinatura Digital](#digital-signature-signing-policy)
-   [Incorporação de uma cadeia de certificados](#embedding-a-certificate-chain)
-   [Usando a estrutura CERT \_ CONTEXT](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Verificando assinaturas digitais em um documento XPS

[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) verifica apenas o conteúdo assinado para determinar que ele não foi alterado desde que foi assinado. **IXpsSignature::Verify** não verifica nenhum dos certificados que foram usados para assinar o conteúdo do documento.

Para obter mais informações sobre certificados e criptografia, consulte [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).

Para ver um exemplo de como verificar assinaturas de documento em um programa, consulte Verificar assinaturas de documento [e certificados.](verify-document-signatures.md)

### <a name="digital-signature-signing-policy"></a>Política de Assinatura Digital

A política de assinatura digital determina quais partes de um documento XPS são assinadas. Uma opção de política de assinatura é assinar as relações de assinatura que começam na parte de origem da assinatura. Como as relações de assinatura mudam com cada assinatura adicionada, as assinaturas feitas nessa política serão quedas quando novas assinaturas são adicionadas. Certifique-se de entender claramente as implicações e os efeitos da configuração dessa política; caso contrário, um comportamento inesperado ou indesejável poderá resultar.

Para obter mais informações sobre políticas de assinatura, consulte [**XPS \_ SIGN \_ POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Incorporação de uma cadeia de certificados

Os certificados que compoem a cadeia de confiança de um certificado específico podem ser adicionados a um documento XPS. A incorporação desses certificados pode facilitar, em cenários fora de linha, para um aplicativo verificar os certificados que uma assinatura digital usa.

Para obter mais informações sobre como inserir certificados em um documento XPS, consulte [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Usando a estrutura CERT \_ CONTEXT

As [**estruturas CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) e [**CERT \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) são as principais estruturas de dados que têm informações de certificado. Para obter mais informações sobre como usar essas estruturas, consulte [Usando uma estrutura de dados CERT \_ INFO](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**CERT \_ As**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) estruturas CONTEXT retornadas pelas funções da API de Criptografia devem ser liberadas quando não são mais necessárias. Para liberar uma **estrutura CERT \_ CONTEXT,** chame a [**função CertFreeCertificateContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Tarefas adicionais de programação de assinatura digital](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**CONTEXTO DO \_ CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**INFORMAÇÕES DE \_ CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**Certfreecertificatecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**POLÍTICA DE \_ ASSINATURA \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
