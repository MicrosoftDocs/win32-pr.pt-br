---
description: Validando a cadeia de certificados
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Validando a cadeia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436513ae9199feb7ba5fcba399537da198ba85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170268"
---
# <a name="validating-the-certificate-chain"></a>Validando a cadeia de certificados

Este tópico descreve como validar a cadeia de certificados do driver ao usar o protocolo COPP (certificado de proteção de saída).

A cadeia de certificados do driver gráfico é um documento XML. A cadeia de certificados contém três certificados. O primeiro certificado é chamado de *certificado de folha* e é o certificado Copp do driver. O próximo certificado é o certificado de autenticação do fornecedor de hardware independente (IHV). O último certificado é o certificado de autenticação da Microsoft. Para garantir que o driver de gráficos seja um dispositivo COPP legítimo, o aplicativo deve validar todos os três certificados. Um programa mal-intencionado pode impedir que o COPP funcione se um aplicativo não validar corretamente os certificados na cadeia.

As cadeias de certificados COPP usam o conjunto de caracteres UTF-8. Os dados binários nos certificados, como a chave pública RSA, são codificados em Base64 e armazenados na ordem big-endian. (*Big-endian* significa que o byte mais significativo é armazenado no local da memória com o endereço mais baixo.)

Alguns elementos dentro de um certificado contêm valores Boolianos para denotar que existe um recurso do certificado. Se o recurso existir, o valor do elemento filho correspondente será definido como 1. Se um recurso não estiver presente, esse elemento filho não estará presente no certificado.

### <a name="xml-element-definitions"></a>Definições de elemento XML

Veja a seguir as definições para elementos no esquema de certificado:

-   **CertificateCollection**. O elemento raiz do documento XML. Ele contém elementos de certificado, um para cada certificado na cadeia.
-   **Certificado**. Contém um certificado. Este elemento contém dados e elementos de assinatura.
-   **Dados**. Contém informações sobre o certificado. Em particular, ele contém a chave pública do certificado e o tipo. O elemento data contém os seguintes elementos filho:
    -   **PublicKey**. Contém a chave pública RSA do certificado. O elemento PublicKey contém um elemento KeyValue, que contém um elemento RSAKeyValue. O elemento RSAKeyValue tem dois elementos filho, módulo e expoente, e eles definem a chave pública. Os elementos de módulo e expoente são codificados na Base64 e armazenados na ordem big-endian.
    -   **Uso** de Key. Se o certificado for o certificado COPP do driver, esse elemento deverá conter um elemento filho chamado EncryptKey. Se o certificado for o certificado de autenticação do IHV ou o certificado de autenticação da Microsoft, ele deverá conter um elemento filho chamado SignCertificate. Ambos os elementos filho contêm valores Boolianos.
    -   **SecurityLevel**. Esse elemento deve ser ignorado.
    -   **ManufacturerData**. Especifica o fabricante e o modelo do dispositivo de gráficos. Este elemento é apenas informativo.
    -   **Recursos**. Contém elementos filho que especificam o uso do certificado. O único relevante para COPP é o elemento COPPCertificate. Outros elementos filho podem estar presentes; Nesse caso, eles devem ser ignorados. Se o elemento COPPCertificate existir, o certificado será um certificado COPP. Esse elemento deve estar presente no nó folha de um certificado COPP válido. Esse elemento contém um valor booliano.
-   **Assinatura**. Contém a assinatura para este certificado. Ele contém os seguintes elementos filho:
    -   **SignedInfo**. Contém informações sobre a assinatura. O elemento filho importante desse elemento é o elemento DigestValue, que contém o valor codificado na base64 do hash SHA-1 sobre o elemento de dados. O valor de Digest é usado ao verificar o certificado em relação à CRL (lista de certificados revogados).
    -   **SignatureValue**. Esse valor é calculado sobre o elemento de dados e é calculado de acordo com o esquema de assinatura digital RSASSA-PSS definido nos padrões de criptografia de Public-Key (PKCS) \# 1 (versão 2,1). Para obter informações sobre o PKCS \# 1, visite [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Contém a chave pública RSA do próximo certificado na cadeia. Esse elemento é usado para verificar se os dados no elemento de dados não foram adulterados. Esse elemento tem o mesmo formato que o elemento PublicKey.

### <a name="certificate-validation"></a>Validação de certificado

O aplicativo deve executar as etapas a seguir para validar corretamente a cadeia de certificados. Se qualquer etapa falhar ou se qualquer elemento mencionado nesses procedimentos não existir, a validação falhará.

### <a name="validate-certificate-collection-procedure"></a>Procedimento para validar a coleção de certificados

Para validar a cadeia de certificados, execute as seguintes etapas:

1.  Verifique se Certificacollection é XML bem formado.
2.  Verifique se Certificacollection está codificado no formato UTF-8.
3.  Verifique se o atributo Version no elemento CertificateCollection é 2,0 ou posterior.
4.  Verifique se a cadeia de certificados contém exatamente três elementos de certificado.
5.  Faça um loop através de cada elemento de certificado na cadeia de certificados e execute o procedimento de validação de certificado, descrito abaixo, em cada um.

### <a name="validate-certificate-procedure"></a>Procedimento de validação de certificado

Para validar um certificado na cadeia, execute as seguintes etapas:

1.  Verifique se nenhum dos elementos filho no elemento de dados está duplicado. Por exemplo, deve haver apenas um elemento PublicKey.
2.  Verifique se o elemento data/PublicKey/KeyValue/RSAKeyValue/módulo existe. O valor decodificado em base64 deve ter 256 bytes de comprimento para todos os certificados, exceto a raiz. No certificado raiz, esse elemento deve ter 128 bytes de comprimento.
3.  Verifique se o elemento data/PublicKey/KeyValue/RSAKeyValue/expoente existe. O valor decodificado em base64 não deve ser maior que 4 bytes.
4.  Se esse certificado for o certificado de folha, verifique o seguinte:
    -   O elemento KeyUsage contém um elemento EncryptKey com o valor 1.
    -   O elemento Features contém um elemento COPPCertificate com o valor 1.
5.  Se esse certificado não for o certificado de folha, verifique o seguinte:
    -   O módulo e o expoente do elemento data/PublicKey correspondem exatamente ao módulo e ao expoente do elemento Signature/KeyInfo do certificado anterior.
    -   O elemento KeyUsage contém um elemento SignCertificate, com o valor 1.
6.  Use o algoritmo de hash SHA-1 para aplicar hash a cada byte no elemento de dados do certificado. Todos os bytes do primeiro caractere na <Data> marca até o último caractere na marca de fechamento </Data> devem ser codificados em hash. O valor de hash é usado para verificar o certificado em relação à CRL (lista de certificados revogados), conforme descrito em [listas de certificados revogados](certificate-revocation-lists.md)
7.  Compare o valor de hash da etapa 6 com o valor decodificado em base64 do elemento Signature/SignedInfo/Reference/DigestValue. Estes valores devem ser correspondentes.
8.  Execute o procedimento de verificação de assinatura, descrito abaixo.
9.  Se esse certificado não for o certificado final na cadeia, salve o valor Signature/KeyInfo/KeyValue/RSAKeyValue para a próxima iteração do loop.
10. Se esse certificado for o certificado final na cadeia, verifique se o valor de Signature/KeyInfo/KeyValue/RSAKeyValue corresponde à chave pública da Microsoft. A chave pública da Microsoft tem os seguintes valores codificados em base64:
    -   Igual

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Lado `AQAB`

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

 

 



