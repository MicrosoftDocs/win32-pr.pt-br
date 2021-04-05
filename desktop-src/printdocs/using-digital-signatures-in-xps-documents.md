---
description: Este tópico lista considerações para usar a API de assinatura digital XPS para adicionar assinaturas digitais a um documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso da API de assinatura digital do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828307"
---
# <a name="using-xps-digital-signature-api"></a>Uso da API de assinatura digital do XPS

Este tópico lista considerações para usar a API de assinatura digital XPS para adicionar assinaturas digitais a um documento XPS.

A API de assinatura digital XPS permite que os aplicativos solicitem aos usuários que assinem documentos XPS e verifiquem as assinaturas encontradas em documentos XPS. A API de assinatura digital XPS pode ser aplicada a um documento XPS sem carregá-lo em um OM XPS e pode ser usada em fluxos de documento XPS que são serializados de um OM XPS.

A seção [tarefas de programação da API de assinatura digital XPS](#xps-digital-signature-api-programming-tasks) contém tópicos que descrevem como programar com a API de assinatura digital XPS. Este tópico lista as seguintes considerações para usar a API de assinatura digital XPS ao adicionar suporte à assinatura digital a um aplicativo.

-   [Tarefas de programação de API de assinatura digital XPS](#xps-digital-signature-api-programming-tasks)
-   [Observações especiais sobre a programação da API de assinatura digital do XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Verificando assinaturas digitais em um documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Política de assinatura de assinatura digital](#digital-signature-signing-policy)
    -   [Inserindo uma cadeia de certificados](#embedding-a-certificate-chain)
    -   [Usando a estrutura de contexto do certificado \_](#using-the-cert\_context-structure)
-   [Tópicos relacionados](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Tarefas de programação de API de assinatura digital XPS

Esta seção contém tópicos que descrevem como executar tarefas de programação usando a API de assinatura digital XPS.

-   [Tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md)<dl>

[Inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md)  
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

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Observações especiais sobre a programação da API de assinatura digital do XPS

Os tópicos a seguir exigem alguma consideração especial quando você usa a API de assinatura digital XPS.

-   [Verificando assinaturas digitais em um documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Política de assinatura de assinatura digital](#digital-signature-signing-policy)
-   [Inserindo uma cadeia de certificados](#embedding-a-certificate-chain)
-   [Usando a estrutura de contexto do certificado \_](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Verificando assinaturas digitais em um documento XPS

[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) verifica apenas o conteúdo assinado para determinar que ele não foi alterado desde que foi assinado. **IXpsSignature:: Verify** não verifica nenhum dos certificados que foram usados para assinar o conteúdo do documento.

Para obter mais informações sobre certificados e criptografia, consulte [sobre criptografia](/windows/desktop/SecCrypto/about-cryptography).

Para obter um exemplo de como verificar assinaturas de documentos em um programa, consulte [verificar assinaturas e certificados de documentos](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Política de assinatura de assinatura digital

A política de assinatura de assinatura digital determina quais partes de um documento XPS são assinadas. Uma opção de política de assinatura é assinar as relações de assinatura que começam da parte de origem da assinatura. Como as relações de assinatura são alteradas com cada assinatura que é adicionada, as assinaturas feitas sob essa política serão interrompidas quando novas assinaturas forem adicionadas. Certifique-se de entender claramente as implicações e os efeitos da definição dessa política; caso contrário, pode ocorrer um comportamento inesperado ou indesejado.

Para obter mais informações sobre diretivas de assinatura, consulte [**\_ \_ política de sinal de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Inserindo uma cadeia de certificados

Os certificados que compõem a cadeia de confiança de um certificado específico podem ser adicionados a um documento XPS. A inserção desses certificados pode facilitar, em cenários off-line, para que um aplicativo Verifique os certificados que uma assinatura digital usa.

Para obter mais informações sobre como inserir certificados em um documento XPS, consulte [Inserir cadeias de certificados em um documento](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Usando a estrutura de contexto do certificado \_

As estruturas de [**\_ informações**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) de certificado e de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado são as principais estruturas de dados que mantêm informações sobre certificados. Para obter mais informações sobre como usar essas estruturas, consulte [usando uma \_ estrutura de dados de informações de certificado](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) As estruturas de contexto que são retornadas pelas funções da API de criptografia devem ser liberadas quando não forem mais necessárias. Para liberar uma estrutura de **\_ contexto de certificado** , chame a função [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Tarefas adicionais de programação de assinatura digital](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**contexto do certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**informações de certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_política de assinatura de XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
