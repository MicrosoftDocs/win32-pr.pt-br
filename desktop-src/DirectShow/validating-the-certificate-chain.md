---
description: Validando a cadeia de certificados
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Validando a cadeia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c63aab8cca71453aff456f145e8f04affd85b4b1f80aa770cbf589970874f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072130"
---
# <a name="validating-the-certificate-chain"></a>Validando a cadeia de certificados

Este tópico descreve como validar a cadeia de certificados do driver ao usar o COPP (Certified Output Protection Protocol).

A cadeia de certificados do driver gráfico é um documento XML. A cadeia de certificados contém três certificados. O primeiro certificado é chamado de *certificado folha* e é o certificado COPP do driver. O próximo certificado é o certificado de assinatura do IHV (Fornecedor Independente de Hardware). O último certificado é o certificado de assinatura da Microsoft. Para garantir que o driver de gráficos seja um dispositivo COPP legítimo, o aplicativo deve validar todos esses três certificados. Um programa mal-intencionado poderá impedir que o COPP funciona se um aplicativo não validar corretamente os certificados na cadeia.

As cadeias de certificados COPP usam o conjunto de caracteres UTF-8. Os dados binários nos certificados, como a chave pública RSA, são codificados em base64 e armazenados em ordem big-endian. (*Big-endian* significa que o byte mais significativo é armazenado no local de memória com o endereço mais baixo.)

Alguns elementos dentro de um certificado contêm valores boolianas para indicar que existe um recurso do certificado. Se o recurso existir, o valor do elemento filho correspondente será definido como 1. Se um recurso não estiver presente, esse elemento filho não estará presente no certificado.

### <a name="xml-element-definitions"></a>Definições de elemento XML

Veja a seguir as definições para elementos no esquema de certificado:

-   **CertificateCollection**. O elemento raiz do documento XML. Ele contém elementos Certificate, um para cada certificado na cadeia.
-   **Certificado**. Contém um certificado. Esse elemento contém elementos Data e Signature.
-   **Dados**. Contém informações sobre o certificado. Em particular, ele contém a chave pública e o tipo do certificado. O elemento Data contém os seguintes elementos filho:
    -   **PublicKey**. Contém a chave pública RSA do certificado. O elemento PublicKey contém um elemento KeyValue, que contém um elemento RSAKeyValue. O elemento RSAKeyValue tem dois elementos filho, Modulus e Exponent, e eles definem a chave pública. Os elementos Modulus e Exponent são codificados em base64 e armazenados em ordem big-endian.
    -   **KeyUsage**. Se o certificado for o certificado COPP do driver, esse elemento deverá conter um elemento filho chamado EncryptKey. Se o certificado for o certificado de assinatura do IHV ou o certificado de assinatura da Microsoft, ele deverá conter um elemento filho chamado SignCertificate. Ambos os elementos filho contêm valores boolianas.
    -   **SecurityLevel**. Esse elemento deve ser ignorado.
    -   **ManufacturerData**. Especifica o fabricante e o modelo do dispositivo gráfico. Esse elemento é apenas informativo.
    -   **Recursos**. Contém elementos filho que especificam o uso do certificado. O único relevante para COPP é o elemento COPPCertificate. Outros elementos filho podem estar presentes; se for o caso, eles deverão ser ignorados. Se o elemento COPPCertificate existir, o certificado será um certificado COPP. Esse elemento deve estar presente no nó folha de um certificado COPP válido. Esse elemento contém um valor booliana.
-   **Assinatura**. Contém a assinatura para esse certificado. Ele contém os seguintes elementos filho:
    -   **SignedInfo**. Contém informações sobre a assinatura. O elemento filho importante desse elemento é o elemento DigestValue, que contém o valor codificado em base64 do hash SHA-1 sobre o elemento Data. O valor de resumo é usado ao verificar o certificado em relação à CRL (lista de certificados revogados).
    -   **SignatureValue.** Esse valor é calculado sobre o elemento Data e é calculado de acordo com o esquema de assinatura digital RSASSA-PSS definido em Public-Key PKCS (Cryptography Standards) \# 1 (versão 2.1). Para obter informações sobre o PKCS \# 1, visite [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Contém a chave pública RSA do próximo certificado na cadeia. Esse elemento é usado para verificar se os dados no elemento Data não foram adulterados. Esse elemento tem o mesmo formato que o elemento PublicKey.

### <a name="certificate-validation"></a>Validação do certificado

O aplicativo deve executar as etapas a seguir para validar corretamente a cadeia de certificados. Se alguma etapa falhar ou se algum elemento referenciado nesses procedimentos não existir, a validação falhará.

### <a name="validate-certificate-collection-procedure"></a>Validar o procedimento de coleta de certificados

Para validar a cadeia de certificados, execute as seguintes etapas:

1.  Verifique se CertificateCollection é XML bem formado.
2.  Verifique se CertificateCollection está codificado no formato UTF-8.
3.  Verifique se o atributo Version no elemento CertificateCollection é 2.0 ou posterior.
4.  Verifique se a cadeia de certificados contém exatamente três elementos Certificate.
5.  Execute um loop em cada elemento Certificate na cadeia de certificados e execute o procedimento Validar Certificado, descrito abaixo, em cada um.

### <a name="validate-certificate-procedure"></a>Validar procedimento de certificado

Para validar um certificado na cadeia, execute as seguintes etapas:

1.  Verifique se nenhum dos elementos filho no elemento Data está duplicado. Por exemplo, deve haver apenas um elemento PublicKey.
2.  Verifique se o elemento Data/PublicKey/KeyValue/RSAKeyValue/Modulus existe. O valor decodificado em base64 deve ter 256 bytes para todos os certificados, exceto a raiz. No certificado raiz, esse elemento deve ter 128 bytes de comprimento.
3.  Verifique se o elemento Data/PublicKey/KeyValue/RSAKeyValue/Exponent existe. O valor decodificado em base64 não deve ser maior que 4 bytes.
4.  Se esse certificado for o certificado folha, verifique o seguinte:
    -   O elemento KeyUsage contém um elemento EncryptKey com o valor 1.
    -   O elemento Features contém um elemento COPPCertificate com o valor 1.
5.  Se esse certificado não for o certificado folha, verifique o seguinte:
    -   O módulo e o expoente do elemento Data/PublicKey exatamente corresponderão ao módulo e ao expoente do elemento Signature/KeyInfo do certificado anterior.
    -   O elemento KeyUsage contém um elemento SignCertificate, com o valor 1.
6.  Use o algoritmo de hash SHA-1 para fazer hash de cada byte no elemento Data do certificado. Cada byte do primeiro caractere na <Data> marca para o último caractere na marca de </Data> fechamento deve ter um hashed. O valor de hash é usado para verificar o certificado em relação à CRL (lista de certificados revogados), conforme descrito em [Listas de Certificados revogados](certificate-revocation-lists.md)
7.  Compare o valor de hash da etapa 6 com o valor decodificado em base64 do elemento Signature/SignedInfo/Reference/DigestValue. Estes valores devem ser correspondentes.
8.  Execute o procedimento Verificar Assinatura, descrito abaixo.
9.  Se esse certificado não for o certificado final na cadeia, salve o valor Signature/KeyInfo/KeyValue/RSAKeyValue para a próxima iteração do loop.
10. Se esse certificado for o certificado final na cadeia, verifique se o valor de Signature/KeyInfo/KeyValue/RSAKeyValue corresponde à chave pública da Microsoft. A chave pública da Microsoft tem os seguintes valores codificados em base64:
    -   Módulo:

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Expoente: `AQAB`

### <a name="verify-signature-procedure"></a>Procedimento de verificação de assinatura

O valor do elemento SignatureValue é calculado sobre o elemento de dados de acordo com o esquema de assinatura digital RSASSA-PSS definido no PKCS \# 1 versão 2,1 (doravante referenciado como Pkcs). Para verificar essa assinatura, execute as seguintes etapas:

1.  Decodifique os valores de módulo e expoente no elemento Signature/KeyInfo/KeyValue/RSAKeyValue. Esses valores definem a chave pública RSA do certificado de autenticação.
2.  Decodifique o elemento Signature/SignatureValue.
3.  Compute a operação RSASSA-PSS-Verify, definida na seção 8.1.2 do PKCS.

Para a operação RSASSA-PSS-Verify, use as seguintes entradas:

-   (*n*,*e*) é a chave pública da etapa 1.
-   *M* é todos os bytes no elemento data, incluindo as marcas <Data> e</Data> que delimitam o elemento.
-   *S* é o valor de assinatura decodificada da etapa 2.

A operação RSASSA-PSS-Verify usa a operação EMSA-PSS-Encode, definida na seção 9.1.1. de PKCS. Para essa operação, a COPP usa as seguintes opções:

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (função de geração de máscara) = MGF1
-   *sLen* = 0

A função de geração de máscara MGF1 é definida no apêndice B. 2 de PKCS. Para essa função, COPP usa as seguintes opções:

-   Hash = SHA-1
-   *hLen* = 20

A saída da operação RSASSA-PSS-Verify indica se a assinatura é válida ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



