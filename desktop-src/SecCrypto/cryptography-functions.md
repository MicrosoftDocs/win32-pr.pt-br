---
description: Lista as funções fornecidas pelo CryptoAPI.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: 'Funções de criptografia '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91338c4a1cea62e2ecc4a2fa1f7254f303ef9b2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104091899"
---
# <a name="cryptography-functions"></a>Funções de criptografia 

As funções de criptografia são categorizadas de acordo com o uso da seguinte maneira:

-   [Funções CryptXML](#cryptxml-functions)
-   [Funções de signatário](#signer-functions)
-   [Funções de criptografia base](#base-cryptography-functions)
    -   [Funções de provedor de serviço](#service-provider-functions)
    -   [Geração de chaves e funções do Exchange](#key-generation-and-exchange-functions)
    -   [Codificação de objeto e funções de decodificação](#object-encoding-and-decoding-functions)
    -   [Criptografia de dados e funções de descriptografia](#data-encryption-and-decryption-functions)
    -   [Funções de hash e assinatura digital](#hash-and-digital-signature-functions)
-   [Funções de repositório de certificados e certificados](#certificate-and-certificate-store-functions)
    -   [Funções de repositório de certificados](#certificate-and-certificate-store-functions)
    -   [Funções de manutenção do repositório de certificados e certificados](#certificate-and-certificate-store-maintenance-functions)
    -   [Funções de certificado](#certificate-functions)
    -   [Funções da lista de certificados revogados](#certificate-revocation-list-functions)
    -   [Funções de lista de certificados confiáveis](#certificate-trust-list-functions)
    -   [Funções de propriedade estendida](#extended-property-functions)
-   [Funções MakeCert](#makecert-functions)
-   [Funções de verificação de certificado](#certificate-verification-functions)
    -   [Funções de verificação usando CTLs](#verification-functions-using-ctls)
    -   [Funções de verificação da cadeia de certificados](#certificate-chain-verification-functions)
-   [Funções de mensagem](#message-functions)
    -   [Funções de mensagem de nível baixo](#low-level-message-functions)
    -   [Funções de mensagens simplificadas](#simplified-message-functions)
-   [Funções auxiliares](#auxiliary-functions)
    -   [Funções de Gerenciamento de Dados](#data-management-functions)
    -   [Funções de conversão de dados](#data-conversion-functions)
    -   [Funções de uso avançado de chave](#enhanced-key-usage-functions)
    -   [Funções de identificador de chave](#key-identifier-functions)
    -   [Funções de suporte a OID](#oid-support-functions)
    -   [Funções de recuperação de objeto remoto](#remote-object-retrieval-functions)
    -   [Funções PFX](#pfx-functions)
-   [Funções de backup e restauração dos serviços de certificados](#certificate-services-backup-and-restore-functions)
-   [Funções de retorno de chamada](#callback-functions)
-   [Funções de definição de catálogo](#catalog-definition-functions)
-   [Funções de catálogo](#catalog-functions)
-   [Funções WinTrust](#wintrust-functions)
-   [Funções do localizador de objeto](#object-locator-functions)

## <a name="cryptxml-functions"></a>Funções CryptXML

As funções XML de criptografia fornecem uma API para criar e representar assinaturas digitais usando dados XML formatados. Para obter informações sobre assinaturas formatadas XML, consulte a sintaxe de XML-Signature e a especificação de processamento em <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Função                                                                          | Descrição                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Um \_ SHAFinal**](a-shafinal.md)                                                 | Computa o hash final dos dados inseridos pela função MD5Update.                                                                                                                                                                                                                                           |
| [**Um \_ SHAInit**](a-shainit.md)                                                   | Inicia o hash de um fluxo de dados.                                                                                                                                                                                                                                                                       |
| [**Um \_ SHAUpdate**](a-shaupdate.md)                                               | Adiciona dados a um objeto hash especificado.                                                                                                                                                                                                                                                                            |
| [**CryptXmlCreateReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Cria uma referência a uma assinatura XML.                                                                                                                                                                                                                                                                         |
| [**CryptXmlAddObject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Adiciona o elemento **Object** à assinatura no contexto do documento aberto para codificação.                                                                                                                                                                                                                        |
| [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Fecha um identificador de objeto XML criptográfico.                                                                                                                                                                                                                                                                        |
| [**CryptXmlDigestReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Usado por um aplicativo para resumir a referência resolvida. Essa função aplica transformações antes de atualizar o resumo.                                                                                                                                                                                            |
| [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Libera o \_ Resumo XML cript \_ . alocado pela função [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest) .                                                                                                                                                                                               |
| [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Cria um objeto de resumo para o método especificado.                                                                                                                                                                                                                                                                |
| [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Analisa o elemento **KeyValue** e cria um identificador de chave de CNG (Cryptography API: Next Generation) BCrypt para verificar uma assinatura.                                                                                                                                                                                   |
| [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Coloca os dados no resumo.                                                                                                                                                                                                                                                                                       |
| [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Codifica os elementos **SignatureMethod** ou **DigestMethod** para algoritmos Agile com parâmetros padrão.                                                                                                                                                                                                           |
| [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Codifica um elemento **KeyValue** .                                                                                                                                                                                                                                                                                  |
| [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Recupera o valor de resumo.                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Decodifica o algoritmo XML e retorna informações sobre o algoritmo.                                                                                                                                                                                                                                           |
| [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Recupera um ponteiro para as funções de extensão criptográficas para o algoritmo especificado.                                                                                                                                                                                                                        |
| [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Assina dados.                                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Verifica uma assinatura.                                                                                                                                                                                                                                                                                            |
| [**CryptXmlEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Codifica dados de assinatura usando a função de retorno de chamada do gravador XML fornecida.                                                                                                                                                                                                                                       |
| [**CryptXmlGetAlgorithmInfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Decodifica a \_ estrutura de algoritmo XML cript \_ e retorna informações sobre o algoritmo.                                                                                                                                                                                                                         |
| [**CryptXmlGetDocContext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Retorna o contexto do documento especificado pelo identificador fornecido.                                                                                                                                                                                                                                                   |
| [**CryptXmlGetReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Retorna o elemento **Reference** especificado pelo identificador fornecido.                                                                                                                                                                                                                                              |
| [**CryptXmlGetSignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Retorna um elemento de **assinatura** XML.                                                                                                                                                                                                                                                                            |
| [**CryptXmlGetStatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Retorna uma estrutura de [**\_ \_ status XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) que contém informações de status sobre o objeto especificado pelo identificador fornecido.                                                                                                                                                           |
| [**CryptXmlGetTransforms**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Retorna informações sobre o mecanismo de cadeia de transformação padrão.                                                                                                                                                                                                                                                    |
| [**CryptXmlImportPublicKey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Importa a chave pública especificada pelo identificador fornecido.                                                                                                                                                                                                                                                         |
| [**CryptXmlOpenToEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Abre uma assinatura digital XML para codificar e retornar um identificador do elemento de **assinatura** aberto. O identificador encapsula um contexto de documento com uma única estrutura de [**\_ \_ assinatura XML criptografada**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) e permanece aberto até que a função [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) seja chamada. |
| [**CryptXmlOpenToDecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Abre uma assinatura digital XML para decodificar e retornar o identificador do contexto do documento que encapsula uma estrutura de [**\_ \_ assinatura XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) . O contexto do documento pode incluir um ou mais elementos de **assinatura** .                                                                 |
| [**CryptXmlSetHMACSecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Define o segredo HMAC no identificador antes de chamar a função [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) ou [**CryptXmlVerify**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature) .                                                                                                                                                        |
| [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Cria uma assinatura criptográfica de um elemento **SignedInfo** .                                                                                                                                                                                                                                                   |
| [**CryptXmlVerifySignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Executa uma validação de assinatura criptográfica de um elemento **SignedInfo** .                                                                                                                                                                                                                                       |
| [*\_retorno de \_ \_ chamada de gravação XML criptografado PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Cria uma transformação para um provedor de dados especificado.                                                                                                                                                                                                                                                               |
| [*\_transformação de \_ criação de XML cript \_ PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Grava dados XML criptográficos.                                                                                                                                                                                                                                                                                   |
| [*\_leitura do \_ \_ provedor de dados XML criptografado PFN \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Lê dados XML criptográficos.                                                                                                                                                                                                                                                                                    |
| [*\_fechamento do \_ \_ provedor de dados XML criptografado PFN \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Libera o provedor de dados XML criptográfico.                                                                                                                                                                                                                                                                    |
| [*\_informações de \_ \_ alg de enumeração XML cript \_ PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Enumera entradas de [**\_ \_ \_ informações de algoritmo XML criptografadas**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) e predefinidas e registradas.                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Funções de signatário

Fornece funções para assinar dados e carimbo de data/hora.



| Função                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SignerFreeSignerContext**](signerfreesignercontext.md) | Libera uma estrutura [**de \_ contexto de signatário**](signer-context.md) alocada por uma chamada anterior à função [**SignerSignEx**](signersignex.md) .                                                                                                                                                                                                                                                                      |
| [**SignError**](signerror.md)                             | Chama a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte o código de retorno em um **HRESULT**.                                                                                                                                                                                                                                                                                                            |
| [**SignerSign**](signersign.md)                           | Assina o arquivo especificado.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SignerSignEx**](signersignex.md)                       | Assina o arquivo especificado e retorna um ponteiro para os dados assinados.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Os sinais e a hora carimbam o arquivo especificado, permitindo várias assinaturas aninhadas.                                                                                                                                                                                                                                                                                                                                      |
| [**SignerTimeStamp**](signertimestamp.md)                 | A hora carimba o assunto especificado. Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) .                                                                                                                                                                                       |
| [**SignerTimeStampEx**](signertimestampex.md)             | Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md). Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) . |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md). Essa função pode ser usada para executar a infraestrutura de chave pública X. 509, em conformidade com a RFC 3161 – carimbos de data/hora.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Time carimba o assunto especificado e dá suporte à configuração de carimbos de data/hora em várias assinaturas.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Funções de criptografia base

As funções criptográficas básicas fornecem o meio mais flexível de desenvolver aplicativos de criptografia. Toda a comunicação com um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ocorre por meio dessas funções.

Um CSP é um módulo independente que executa todas as operações de criptografia. Pelo menos um CSP é necessário com cada aplicativo que usa funções criptográficas. Um único aplicativo pode, ocasionalmente, usar mais de um CSP.

Se mais de um CSP for usado, o que será usado poderá ser especificado nas chamadas de função criptográficas do CryptoAPI. Um CSP, o Microsoft Base Cryptographic Provider, é fornecido com o [*CryptoAPI*](../secgloss/c-gly.md). Esse CSP é usado como um provedor padrão por muitas das funções de CryptoAPI se nenhum outro CSP for especificado.

Cada CSP fornece uma implementação diferente do suporte de criptografia fornecido ao CryptoAPI. Alguns fornecem algoritmos criptográficos mais fortes; outras contêm componentes de hardware, como [*cartões inteligentes*](../secgloss/s-gly.md). Além disso, alguns CSPs podem ocasionalmente se comunicar diretamente com os usuários, como quando as [*assinaturas digitais*](../secgloss/d-gly.md) são executadas usando a [*chave privada de assinatura*](../secgloss/s-gly.md)do usuário.

As funções de criptografia base estão nos seguintes grupos amplos:

-   Funções de provedor de serviço
-   Geração de chaves e funções do Exchange
-   Codificação de objeto e funções de decodificação
-   Criptografia de dados e funções de descriptografia
-   Funções de hash e assinatura digital

### <a name="service-provider-functions"></a>Funções de provedor de serviço

Os aplicativos usam as funções de serviço a seguir para se conectar e desconectar um [*provedor de serviços de criptografia*](../secgloss/c-gly.md) (CSP).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Adquire um identificador para o <a href="/windows/desktop/SecGloss/k-gly"><em>contêiner de chave</em></a> do usuário atual em um CSP específico.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>CryptContextAddRef</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Incrementa a <a href="/windows/desktop/SecGloss/r-gly"><em>contagem de referência</em></a> em um identificador <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>CryptEnumProviders</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Enumera os provedores em um computador.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>CryptEnumProviderTypes</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Enumera os tipos de provedores com suporte no computador.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>CryptGetDefaultProvider</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Determina o CSP padrão para o usuário atual ou para o computador para um tipo de provedor especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Recupera os parâmetros que regem as operações de um CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Instala um contexto <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> adquirido anteriormente para ser usado como um contexto padrão.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>CryptReleaseContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Libera o identificador adquirido pela função <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>CryptSetProvider</strong></a> e <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>CryptSetProviderEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Especifica o CSP padrão do usuário para um tipo de CSP específico.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>CryptSetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Especifica os atributos de um CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>CryptUninstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Remove um contexto padrão instalado anteriormente pelo <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>FreeCryptProvFromCertEx</strong></a></td>
<td>Libera o identificador para um CSP ( <a href="/windows/desktop/SecGloss/c-gly"><em>provedor de serviços de criptografia</em></a> ) ou para uma chave de Cryptography API: próxima geração (CNG).</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>Geração de chaves e funções do Exchange

As funções de geração de chave e troca [*trocam chaves*](../secgloss/e-gly.md) com outros usuários e criam, configuram e destruim [*chaves criptográficas*](../secgloss/c-gly.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>CryptDeriveKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Cria uma chave derivada de uma senha.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>CryptDestroyKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Destrói uma chave.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>CryptDuplicateKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Faz uma cópia exata de uma chave, incluindo o <a href="/windows/desktop/SecGloss/s-gly"><em>estado</em></a> da chave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Transfere uma chave do CSP para um <a href="/windows/desktop/SecGloss/k-gly"><em>blob de chave</em></a> no espaço de memória do aplicativo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Cria uma chave aleatória.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Gera dados aleatórios.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>CryptGetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Recupera os parâmetros de uma chave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Obtém um identificador para a chave de assinatura ou troca de chaves.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>CryptImportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Transfere uma chave de um <a href="/windows/desktop/SecGloss/k-gly"><em>blob de chave</em></a> para um CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Especifica os parâmetros de uma chave.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Codificação de objeto e funções de decodificação

Essas são funções generalizadas de codificação e decodificação. Eles são usados para codificar e decodificar [*certificados*](../secgloss/c-gly.md), listas de certificados [*revogados*](../secgloss/c-gly.md) (CRLs), [*solicitações de certificado*](../secgloss/c-gly.md)e extensões de certificado.

| Função                                           | Descrição                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Decodifica uma estrutura do tipo *lpszStructType*.                                                                                                    |
| [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Decodifica uma estrutura do tipo *lpszStructType*. [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) dá suporte à opção de alocação de memória de passagem única. |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Codifica uma estrutura do tipo *lpszStructType*.                                                                                                    |
| [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Codifica uma estrutura do tipo *lpszStructType*. [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) dá suporte à opção de alocação de memória de passagem única. |



 

### <a name="data-encryption-and-decryption-functions"></a>Criptografia de dados e funções de descriptografia

As funções a seguir dão suporte a operações de criptografia e descriptografia. [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) e [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) exigem uma [*chave criptográfica*](../secgloss/c-gly.md) antes de serem chamadas. Isso é feito usando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)ou [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . O algoritmo de criptografia é especificado quando a chave é criada. [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) pode definir parâmetros de criptografia adicionais.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>CryptDecrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Descriptografa uma seção de <a href="/windows/desktop/SecGloss/c-gly"><em>texto cifrado</em></a> usando a chave de criptografia especificada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Criptografa uma seção de <a href="/windows/desktop/SecGloss/p-gly"><em>texto não criptografado</em></a> usando a chave de criptografia especificada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Executa a criptografia nos dados em uma estrutura de <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>Criptografa a memória para proteger informações confidenciais.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Executa uma descriptografia e verificação de integridade dos dados em um <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>Descriptografa a memória que foi criptografada usando <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a>.</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Funções de hash e assinatura digital

Essas funções computam [*hashes*](../secgloss/h-gly.md) de dados e também criam e verificam [*assinaturas digitais*](../secgloss/d-gly.md). Os hashes também são conhecidos como resumos de mensagens.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Cria um objeto hash vazio.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>CryptDestroyHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Destrói um objeto de hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>CryptDuplicateHash</strong></a></td>
<td>Duplica um objeto de hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>Recupera um parâmetro de objeto de hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Aplica hash a um bloco de dados, adicionando-o ao objeto hash especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>CryptHashSessionKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Aplica hash a uma chave de sessão, adicionando-a ao objeto hash especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>CryptSetHashParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Define um parâmetro de objeto de hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>CryptSignHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Assina o objeto hash especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a></td>
<td>Exibe um assistente que assina digitalmente um documento ou um <a href="/windows/desktop/SecGloss/b-gly"><em>blob</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>CryptUIWizFreeDigitalSignContext</strong></a></td>
<td>Libera um ponteiro para uma estrutura de <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>CryptVerifySignature</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Verifica uma assinatura digital, dado um identificador ao objeto de hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>PFNCFILTERPROC</strong></a></td>
<td>Filtra os certificados que aparecem no assistente de assinatura digital exibido pela função <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Funções de repositório de certificados e certificados

As funções de repositório de certificados e certificados gerenciam o uso, o armazenamento e a recuperação de [*certificados*](../secgloss/c-gly.md), CRLs (listas de certificados [*revogados*](../secgloss/c-gly.md) ) e [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs). Essas funções são divididas nos seguintes grupos:

-   Funções de repositório de certificados
-   Funções de manutenção do repositório de certificados e certificados
-   Funções de certificado
-   Funções da lista de certificados revogados
-   Funções de lista de certificados confiáveis
-   Funções de propriedade estendida
-   Funções MakeCert

### <a name="certificate-store-functions"></a>Funções de repositório de certificados

Um site de usuário pode, ao longo do tempo, coletar muitos certificados. Normalmente, um site tem certificados para o usuário do site, bem como outros certificados que descrevem aqueles indivíduos e entidades com quem o usuário se comunica. Para cada entidade, pode haver mais de um certificado. Para cada certificado individual, deve haver uma cadeia de verificação de certificados que fornece uma trilha de volta para um [*certificado raiz*](../secgloss/r-gly.md)confiável. Os [*repositórios de certificados*](../secgloss/c-gly.md) e suas funções relacionadas fornecem funcionalidade para armazenar, recuperar, enumerar, verificar e usar as informações armazenadas nos certificados.

| Função                                                               | Descrição                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Adiciona um repositório de certificados irmãos a um repositório de certificados de coleção.                                                                                                                                                                                                                                                                       |
| [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Fecha um identificador de repositório de certificados.                                                                                                                                                                                                                                                                                                        |
| [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Permite que um aplicativo seja notificado quando há uma diferença entre o conteúdo de um armazenamento em cache e o conteúdo do armazenamento que é persistido no armazenamento. Ele também fornece a dessincronização do armazenamento em cache, se necessário, e fornece um meio de confirmar as alterações feitas no armazenamento armazenado em cache para o repositório persistente.<br/> |
| [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Duplica um identificador de repositório aumentando a contagem de [*referência*](../secgloss/r-gly.md).                                                                                                                                                                                            |
| [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Enumera os repositórios físicos para um repositório do sistema especificado.                                                                                                                                                                                                                                                                              |
| [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Enumera todos os armazenamentos do sistema disponíveis.                                                                                                                                                                                                                                                                                                   |
| [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Enumera todos os locais que têm um armazenamento do sistema disponível.                                                                                                                                                                                                                                                                      |
| [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Obtém uma propriedade de repositório.                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Abre um repositório de certificados usando um tipo de provedor de armazenamento especificado.                                                                                                                                                                                                                                                                          |
| [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Abre um repositório de certificados do sistema com base em um protocolo de subsistema.                                                                                                                                                                                                                                                                           |
| [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Adiciona um repositório físico a uma coleção do repositório do sistema do registro.                                                                                                                                                                                                                                                                              |
| [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Registra um repositório do sistema.                                                                                                                                                                                                                                                                                                                 |
| [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Remove um repositório de certificados irmãos de um repositório de coleta.                                                                                                                                                                                                                                                                              |
| [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Salva o repositório de certificados.                                                                                                                                                                                                                                                                                                              |
| [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Define uma propriedade de repositório.                                                                                                                                                                                                                                                                                                                    |
| [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Remove um repositório físico de uma coleção de repositório do sistema especificada.                                                                                                                                                                                                                                                                        |
| [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Cancela o registro de um repositório do sistema especificado.                                                                                                                                                                                                                                                                                                     |
| [**CryptUIWizExport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Apresenta um assistente que exporta um certificado, a CTL (lista de certificados confiáveis), a CRL (lista de certificados revogados) ou o repositório de certificados.                                                                                                                                                                                                      |
| [**CryptUIWizImport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Apresenta um assistente que importa um certificado, a CTL (lista de certificados confiáveis), a CRL (lista de certificados revogados) ou o repositório de certificados.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Funções de manutenção do repositório de certificados e certificados

O CryptoAPI fornece um conjunto de funções gerais de manutenção do repositório de certificados e certificados.

| Função                                                                                                                              | Descrição                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Adiciona o certificado serializado ou o elemento CRL ao repositório.                                   |
| [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Cria o contexto especificado a partir dos bytes codificados. O novo contexto não é colocado em um repositório. |
| [**CertEnumSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Enumera o TrustedSubjects em um contexto de CTL classificado.                                        |
| [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Localiza o assunto especificado em uma CTL.                                                          |
| [**CertFindSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Localiza o assunto especificado em uma CTL classificada.                                                   |
| [**OpenPersonalTrustDBDialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) e [ **OpenPersonalTrustDBDialogEx**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Exibe a caixa de diálogo **certificados** .                                                      |



 

### <a name="certificate-functions"></a>Funções de certificado

A maioria das funções de [*certificado*](../secgloss/c-gly.md) tem funções relacionadas para lidar com [*CRLs*](../secgloss/c-gly.md) e [*CTLs*](../secgloss/c-gly.md). Para obter mais informações sobre as funções de CRL e CTL relacionadas, consulte funções de lista de certificados revogados e funções de lista de certificados confiáveis.

| Função                                                                             | Descrição                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Adiciona um contexto de certificado ao repositório de certificados.                                                                                                                                                                                            |
| [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Adiciona um link em um repositório de certificados a um contexto de certificado em um repositório diferente.                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Converte o certificado codificado em um contexto de certificado e, em seguida, adiciona o contexto ao repositório de certificados.                                                                                                                                  |
| [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Incrementa a contagem de referência para um identificador de **\_ \_ \_ resposta OCSP do servidor HCERT** .                                                                                                                                                                 |
| [**CertAddRefServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Incrementa a contagem de referência para uma estrutura de [**\_ \_ \_ \_ contexto de resposta OCSP do servidor de CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context) .                                                                                                              |
| [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Fecha um identificador de resposta do servidor OCSP ( [*protocolo de status de certificado online*](../secgloss/o-gly.md) ).                                               |
| [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Cria um contexto de certificado a partir de um certificado codificado. O contexto criado não é colocado em um repositório de certificados.                                                                                                                               |
| [**CertCreateSelfSignCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | Cria um certificado autoassinado.                                                                                                                                                                                                              |
| [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Exclui um certificado do repositório de certificados.                                                                                                                                                                                               |
| [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Duplica um contexto de certificado incrementando sua [*contagem de referência*](../secgloss/r-gly.md).                                                                                           |
| [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Enumera os contextos de certificado no repositório de certificados.                                                                                                                                                                                   |
| [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Localiza o primeiro, ou próximo, o contexto de certificado no repositório de certificados que atende a um critério de pesquisa.                                                                                                                                           |
| [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Libera um contexto de certificado.                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Obtém um contexto de certificado do repositório de certificados para o primeiro, ou próximo, emissor do certificado de entidade especificado.                                                                                                                      |
| [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Recupera um contexto de resposta OCSP ( [*protocolo de status de certificado online*](../secgloss/o-gly.md) ) válido de não bloqueio para o identificador especificado. |
| [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Obtém do repositório de certificados o contexto do certificado do assunto, que é identificado exclusivamente por seu emissor e número de série.                                                                                                                  |
| [**CertGetValidUsages**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Retorna uma matriz de usos que consiste na interseção de usos válidos para todos os certificados em uma matriz de certificados.                                                                                                               |
| [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Abre um identificador para uma resposta OCSP ( [*protocolo de status de certificado online*](../secgloss/o-gly.md) ) associada a uma cadeia de certificados de servidor.       |
| [**CertRetrieveLogoOrBiometricInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Executa uma recuperação de URL do logotipo ou das informações biométricas especificadas na extensão do certificado **szOID \_ logotipo \_ ext** ou **szOID \_ Biometric \_** .                                                                                  |
| [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Apresenta uma caixa de diálogo que permite ao usuário selecionar certificados de um conjunto de certificados que correspondem a um determinado critério.                                                                                                                       |
| [**CertSelectCertificateChains**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Recupera cadeias de certificados com base em critérios de seleção especificados.                                                                                                                                                                             |
| [**CertSelectionGetSerializedBlob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Uma função auxiliar usada para recuperar um [*blob*](../secgloss/b-gly.md) de certificado serializado de uma estrutura de [**\_ \_ entrada SELECTUI de certificado**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input) .                                               |
| [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Serializa o certificado codificado de um contexto de certificado e uma representação codificada de suas propriedades.                                                                                                                                         |
| [**CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Executa as verificações de verificação habilitadas no certificado do assunto usando o emissor.                                                                                                                                                           |
| [**CryptUIDlgCertMgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Exibe uma caixa de diálogo que permite ao usuário gerenciar certificados.                                                                                                                                                                              |
| [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)                   | Exibe uma caixa de diálogo que permite que um usuário selecione um certificado.                                                                                                                                                                               |
| [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Exibe uma caixa de diálogo que permite a seleção de um certificado de um repositório especificado.                                                                                                                                                        |
| [**CryptUIDlgViewCertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Apresenta uma caixa de diálogo que exibe um certificado especificado.                                                                                                                                                                                    |
| [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Exibe um certificado, CRL ou CTL.                                                                                                                                                                                                            |
| [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)                         | Exibe uma caixa de diálogo que contém as informações de signatário de uma mensagem assinada.                                                                                                                                                                |
| [**GetFriendlyNameOfCert**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Recupera o nome de exibição de um certificado.                                                                                                                                                                                                   |
| [**RKeyCloseKeyService**](rkeyclosekeyservice.md)                                   | Fecha um identificador de serviço de chave.                                                                                                                                                                                                                    |
| [**RKeyOpenKeyService**](rkeyopenkeyservice.md)                                     | Abre um identificador de serviço de chave em um computador remoto.                                                                                                                                                                                                |
| [**RKeyPFXInstall**](rkeypfxinstall.md)                                             | Instala um certificado em um computador remoto.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Funções da lista de certificados revogados

Essas funções gerenciam o armazenamento e a recuperação de [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs).

| Função                                                             | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Adiciona um contexto de CRL ao repositório de certificados.                                                                                                                                          |
| [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Adiciona um link em uma loja a um contexto de CRL em um repositório diferente.                                                                                                                         |
| [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Converte a CRL codificada em um contexto de CRL e, em seguida, adiciona o contexto ao repositório de certificados.                                                                                        |
| [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Cria um contexto de CRL de uma CRL codificada. O contexto criado não é colocado em um repositório de certificados.                                                                                     |
| [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Exclui uma CRL do repositório de certificados.                                                                                                                                             |
| [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Duplica um contexto de CRL incrementando a [*contagem de referência*](../secgloss/r-gly.md).                                         |
| [**CertEnumCRLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Enumera os contextos de CRL em um repositório.                                                                                                                                               |
| [**CertFindCertificateInCRL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Pesquisa a CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) do certificado especificado. |
| [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Localiza o primeiro, ou próximo, o contexto de CRL no repositório de certificados que corresponde a um critério específico.                                                                                     |
| [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Libera um contexto de CRL.                                                                                                                                                                  |
| [**CertGetCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Obtém o primeiro, ou próximo, o contexto de CRL do repositório de certificados para o certificado de emissor especificado.                                                                                 |
| [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Serializa a CRL codificada do contexto de CRL e suas propriedades.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Funções de lista de certificados confiáveis

Essas funções gerenciam o armazenamento e a recuperação de [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs).

| Função                                                               | Descrição                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Adiciona um contexto de CTL ao repositório de certificados.                                                                         |
| [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Adiciona um link em uma loja a um contexto de CRL em um repositório diferente.                                                        |
| [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Converte a CTL codificada em um contexto de CTL e, em seguida, adiciona o contexto ao repositório de certificados.                       |
| [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Cria um contexto de CTL a partir de uma lista de certificados confiáveis codificados. O contexto criado não é colocado em um repositório de certificados. |
| [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Exclui uma CTL do repositório de certificados.                                                                            |
| [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Duplica um contexto de CTL incrementando a contagem de referência.                                                        |
| [**CertEnumCTLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Enumera os contextos de CTL no repositório de certificados.                                                                |
| [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Localiza o primeiro contexto de CTL, ou próximo, no repositório de certificados que corresponde a um critério específico.                     |
| [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Libera um contexto de CTL.                                                                                                 |
| [**CertModifyCertificatesToTrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Modifica o conjunto de certificados em uma CTL para uma determinada finalidade.                                                       |
| [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Serializa a CTL codificada do contexto de CTL e suas propriedades.                                                         |



 

### <a name="extended-property-functions"></a>Funções de propriedade estendida

As funções a seguir funcionam com propriedades estendidas de certificados, CRLs e CTLs.

| Função                                                                             | Descrição                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Enumera as propriedades para o contexto de certificado especificado. |
| [**CertEnumCRLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Enumera as propriedades para o contexto de CRL especificado.         |
| [**CertEnumCTLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Enumera as propriedades para o contexto de CTL especificado.         |
| [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Recupera as propriedades do certificado.                                |
| [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Recupera as propriedades da CRL.                                        |
| [**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Recupera as propriedades da CTL.                                        |
| [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Define as propriedades do certificado.                                     |
| [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Define as propriedades da CRL.                                             |
| [**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Define propriedades de CTL.                                             |



 

## <a name="makecert-functions"></a>Funções MakeCert

As funções a seguir dão suporte à ferramenta [MakeCert](makecert.md) .



| Função                                                                               | Descrição                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCryptProvFromCert**](freecryptprovfromcert.md)                                 | Libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e, opcionalmente, exclui o contêiner temporário criado pela função [**GetCryptProvFromCert**](getcryptprovfromcert.md) . |
| [**GetCryptProvFromCert**](getcryptprovfromcert.md)                                   | Obtém um identificador para um CSP e uma especificação de chave para um contexto de certificado.                                                                                                                                                                                                                                |
| [**PvkFreeCryptProv**](pvkfreecryptprov.md)                                           | Libera o identificador para um CSP e, opcionalmente, exclui o contêiner temporário criado pela função [**PvkGetCryptProv**](pvkgetcryptprov.md) .                                                                                                                                                          |
| [**PvkGetCryptProv**](pvkgetcryptprov.md)                                             | Obtém um identificador para um CSP com base em um nome de arquivo de [*chave privada*](../secgloss/p-gly.md) ou em um nome de contêiner de chave.                                                                                                                                          |
| [**PvkPrivateKeyAcquireContextFromMemory**](pvkprivatekeyacquirecontextfrommemory.md) | Cria um contêiner temporário no CSP e carrega uma chave privada da memória no contêiner.                                                                                                                                                                                                         |
| [**PvkPrivateKeySave**](pvkprivatekeysave.md)                                         | Salva uma chave privada e sua [*chave pública*](../secgloss/p-gly.md) correspondente em um arquivo especificado.                                                                                                                                                          |
| [**SignError**](signerror.md)                                                         | Chama [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte o código de retorno em um **HRESULT**.                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Funções de verificação de certificado

Os certificados são verificados usando as cadeias de certificados ou [*CTLs*](../secgloss/c-gly.md) . As funções são fornecidas para ambos:

-   Funções de verificação usando CTLs
-   Funções de verificação da cadeia de certificados

### <a name="verification-functions-using-ctls"></a>Funções de verificação usando CTLs

Essas funções usam CTLs no processo de verificação. Funções adicionais para trabalhar com CTLs podem ser encontradas em funções de lista de certificados confiáveis e funções de propriedade estendidas.

As funções a seguir usam CTLs diretamente para verificação.

| Função                                                         | Descrição                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Verifica o uso de uma CTL.                 |
| [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Codifica e assina uma CTL como uma mensagem.        |
| [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Recupera e verifica uma CTL de uma mensagem. |
| [**CryptMsgSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Assina uma mensagem que contém uma CTL.         |



 

### <a name="certificate-chain-verification-functions"></a>Funções de verificação da cadeia de certificados

As cadeias de certificados são criadas para fornecer informações de confiança sobre certificados individuais.

| Nome da função                                                                                                    | Descrição                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Cria um novo mecanismo de cadeia não padrão para um aplicativo.                                                                                                                                                          |
| [**CertCreateCTLEntryFromCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Cria uma entrada de CTL cujos atributos são as propriedades do contexto de certificado.                                                                                                                                      |
| [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Duplica uma cadeia de certificados incrementando a [*contagem de referência*](../secgloss/r-gly.md) da cadeia e retornando um ponteiro para a cadeia.                    |
| [**CertFindChainInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Localiza o primeiro, ou próximo, o contexto da cadeia de certificados em um repositório.                                                                                                                                                     |
| [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Libera uma cadeia de certificados reduzindo sua contagem de referência.                                                                                                                                                          |
| [**CertFreeCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Libera um mecanismo de cadeia de certificados não padrão.                                                                                                                                                                        |
| [**CertFreeCertificateChainList**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Libera a matriz de ponteiros para contextos de cadeia.                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Cria um contexto de cadeia a partir de um certificado final e voltando para um [*certificado raiz*](../secgloss/r-gly.md)confiável, se possível.                |
| [**CertIsValidCRLForCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Verifica uma [*CRL*](../secgloss/c-gly.md) para determinar se ela deve incluir um certificado específico se o certificado fosse revogado. |
| [**CertSetCertificateContextPropertiesFromCTLEntry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Define propriedades no contexto do certificado usando os atributos na entrada de CTL.                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Verifica uma cadeia de certificados para verificar sua validade, incluindo sua conformidade com quaisquer critérios de política de validade especificados.                                                                                            |



 

## <a name="message-functions"></a>Funções de mensagem

As funções de mensagem do [*CryptoAPI*](../secgloss/c-gly.md) consistem em dois grupos de funções: funções de mensagens de nível baixo e [*funções de mensagens simplificadas*](../secgloss/s-gly.md).

As funções de mensagens de nível baixo criam e trabalham diretamente com \# mensagens PKCS 7. Essas funções codificam \# dados PKCS 7 para transmissão e decodificam \# dados PKCS 7 recebidos. Eles também descriptografam e verificam as assinaturas de mensagens recebidas. Para obter uma visão geral das \# mensagens padrão e de baixo nível do PKCS 7, consulte [mensagens de nível inferior](low-level-messages.md).

As funções de mensagens simplificadas estão em um nível mais alto e encapsulam várias funções de mensagens de nível baixo e funções de certificado em funções únicas que executam uma tarefa específica de uma maneira específica. Essas funções reduzem o número de chamadas de função necessárias para realizar uma tarefa, simplificando assim o uso do CryptoAPI. Para obter uma visão geral das mensagens simplificadas, consulte [mensagens simplificadas](simplified-messages.md).

-   Funções de mensagem de nível baixo
-   Funções de mensagens simplificadas

### <a name="low-level-message-functions"></a>Funções de mensagem de nível baixo

As funções de mensagens de nível baixo fornecem a funcionalidade necessária para codificar dados para transmissão e decodificar \# mensagens PKCS 7 recebidas. A funcionalidade também é fornecida para descriptografar e verificar as assinaturas de mensagens recebidas. O uso dessas funções de mensagens de baixo nível na maioria dos aplicativos não é recomendado. Para a maioria dos aplicativos, o uso de funções de mensagens simplificadas, que encapsulam várias funções de mensagens de baixo nível em uma única chamada de função, é preferencial.

| Função                                                                                   | Descrição                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Calcula o comprimento de uma mensagem criptográfica codificada.                                                                                                                                                                     |
| [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Fecha um identificador de uma mensagem criptográfica.                                                                                                                                                                                    |
| [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Executa uma função de controle especial após a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) final de uma mensagem criptográfica codificada ou decodificada.                                                                                   |
| [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Referendas uma assinatura já existente em uma mensagem.                                                                                                                                                                       |
| [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Referendas uma assinatura já existente (codificada SignerInfo, conforme definido pelo PKCS \# 7).                                                                                                                                       |
| [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Duplica um identificador de mensagem criptográfica incrementando a [*contagem de referência*](../secgloss/r-gly.md). A contagem de referência mantém o controle do tempo de vida da mensagem. |
| [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Adquire um parâmetro após a codificação ou decodificação de uma mensagem criptográfica.                                                                                                                                                       |
| [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Abre uma mensagem de criptografia para decodificação.                                                                                                                                                                                    |
| [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Abre uma mensagem de criptografia para codificação.                                                                                                                                                                                    |
| [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Atualiza o conteúdo de uma mensagem de criptografia.                                                                                                                                                                               |
| [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Verifica uma [*referenda*](../secgloss/c-gly.md) em termos da estrutura SignerInfo (conforme definido pelo PKCS \# 7).                                                   |
| [**CryptMsgVerifyCountersignatureEncodedEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Verifica se o parâmetro *pbSignerInfoCounterSignature* contém o [*hash*](../secgloss/h-gly.md) criptografado do campo **EncryptedDigest** da estrutura de parâmetro *pbSignerInfo* .   |



 

### <a name="simplified-message-functions"></a>Funções de mensagens simplificadas

as [*funções de mensagens simplificadas*](../secgloss/s-gly.md) encapsulam funções de mensagens de nível baixo em uma única função para realizar uma tarefa especificada.

| Função                                                                               | Descrição                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Decodifica uma mensagem criptográfica.                                                                                                                                                                                                                                             |
| [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Descriptografa a mensagem especificada e verifica o signatário.                                                                                                                                                                                                                     |
| [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Descriptografa a mensagem especificada.                                                                                                                                                                                                                                              |
| [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Criptografa a mensagem para o destinatário ou destinatários.                                                                                                                                                                                                                        |
| [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Retorna o [*repositório de certificados*](../secgloss/c-gly.md) que contém os certificados e as [*CRLs*](../secgloss/c-gly.md)da mensagem. |
| [**CryptGetMessageSignerCount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Retorna a contagem de assinantes na mensagem assinada.                                                                                                                                                                                                                          |
| [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Cria um hash da mensagem.                                                                                                                                                                                                                                               |
| [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Assina a mensagem e, em seguida, a criptografa para o destinatário ou destinatários.                                                                                                                                                                                                     |
| [**CryptSignMessageWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Assina uma mensagem usando a chave privada do CSP especificada nos parâmetros para a função.                                                                                                                                                                                       |
| [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Assina a mensagem.                                                                                                                                                                                                                                                           |
| [**CryptVerifyDetachedMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Verifica uma mensagem com hash que contém um hash desanexado.                                                                                                                                                                                                                     |
| [**CryptVerifyDetachedMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Verifica uma mensagem assinada que contém uma assinatura desanexada ou assinaturas.                                                                                                                                                                                                  |
| [**CryptVerifyMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Verifica uma mensagem com hash.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Verifica uma mensagem assinada.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignatureWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Verifica a assinatura de uma mensagem assinada usando informações de chave pública especificadas.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Funções auxiliares

As funções auxiliares são agrupadas da seguinte maneira:

-   Funções de Gerenciamento de Dados
-   Funções de conversão de dados
-   Funções de uso avançado de chave
-   Funções de identificador de chave
-   Funções de suporte a OID
-   Funções de recuperação de objeto remoto
-   Funções PFX

### <a name="data-management-functions"></a>Funções de Gerenciamento de Dados

As funções CryptoAPI a seguir gerenciam dados e certificados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>CertCompareCertificate</strong></a></td>
<td>Compara dois certificados para determinar se eles são idênticos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>CertCompareCertificateName</strong></a></td>
<td>Compara dois nomes de certificado para determinar se eles são idênticos.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>CertCompareIntegerBlob</strong></a></td>
<td>Compara dois <a href="/windows/desktop/SecGloss/b-gly"><em>BLOBs</em></a>inteiros.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>CertComparePublicKeyInfo</strong></a></td>
<td>Compara duas <a href="/windows/desktop/SecGloss/p-gly"><em>chaves públicas</em></a> para determinar se elas são idênticas.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>CertFindAttribute</strong></a></td>
<td>Localiza o primeiro atributo identificado por seu OID ( <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> ).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>CertFindExtension</strong></a></td>
<td>Localiza a primeira extensão identificada por seu OID.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>CertFindRDNAttr</strong></a></td>
<td>Localiza o primeiro atributo <a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a> identificado por seu OID na lista nome dos <em>nomes distintos relativos</em>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>CertGetIntendedKeyUsage</strong></a></td>
<td>Adquire os bytes de uso de chave pretendidos do certificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>CertGetPublicKeyLength</strong></a></td>
<td>Adquire o comprimento de bit da chave pública/privada do <a href="/windows/desktop/SecGloss/p-gly"><em>blob de chave pública</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>CertIsRDNAttrsInCertificateName</strong></a></td>
<td>Compara os atributos no <a href="/windows/desktop/SecGloss/c-gly"><em>nome do certificado</em></a> com o <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>CERT_RDN</strong></a> especificado para determinar se todos os atributos estão incluídos lá.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>CertIsStrongHashToSign</strong></a></td>
<td>Determina se o algoritmo de hash especificado e a chave pública no certificado de autenticação podem ser usados para executar a assinatura forte.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>CertVerifyCRLRevocation</strong></a></td>
<td>Verifica se o certificado do requerente não está na CRL ( <a href="/windows/desktop/SecGloss/c-gly"><em>lista de certificados revogados</em></a> ).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>CertVerifyCRLTimeValidity</strong></a></td>
<td>Verifica a validade de tempo de uma CRL.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>CertVerifyRevocation</strong></a></td>
<td>Verifica se o certificado do requerente não está na CRL.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>CertVerifyTimeValidity</strong></a></td>
<td>Verifica a validade do tempo de um certificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>CertVerifyValidityNesting</strong></a></td>
<td>Verifica se a validade da hora da entidade está aninhada na validade do tempo do emissor.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Essa função é substituída pela função <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Exporta a chave privada no formato de #8 PKCS.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>Exporta as informações de chave pública associadas à chave privada correspondente do provedor.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>CryptExportPublicKeyInfoEx</strong></a></td>
<td>Exporta as informações de chave pública associadas à chave privada correspondente do provedor. Essa função é diferente de <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> , pois o usuário pode especificar o algoritmo de chave pública, substituindo, assim, o padrão fornecido pelo CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>CryptExportPublicKeyInfoFromBCryptKeyHandle</strong></a></td>
<td>Exporta as informações de chave pública associadas à chave privada correspondente de um provedor.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>CryptFindCertificateKeyProvInfo</strong></a></td>
<td>Enumera os provedores criptográficos e seus <a href="/windows/desktop/SecGloss/k-gly"><em>contêineres de chave</em></a> para localizar a chave privada que corresponde à chave pública de um certificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>CryptFindLocalizedName</strong></a></td>
<td>Localiza o nome localizado para um nome especificado, por exemplo, localiza o nome localizado para o nome da loja do sistema raiz.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>CryptHashCertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Aplica hash ao conteúdo codificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Aplica hash a um bloco de dados usando um provedor de hash de API de criptografia: próxima geração (CNG).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>CryptHashPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Computa o hash das informações de chave pública codificadas.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>CryptHashToBeSigned</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Computa o hash do &quot; para receber &quot; informações no conteúdo assinado codificado (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Importa a <a href="/windows/desktop/SecGloss/p-gly"><em>chave privada</em></a> no formato de #8 PKCS para um CSP ( <a href="/windows/desktop/SecGloss/c-gly"><em>provedor de serviços de criptografia</em></a> ).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Converte e importa informações de chave pública para o provedor e retorna um identificador da chave pública.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Converte e importa as informações de chave pública para o provedor e retorna um identificador da chave pública. Parâmetros adicionais (sobre aqueles especificados por <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a>) que podem ser usados para substituir os padrões são fornecidos para <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>suplementares.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Importa uma chave pública para um provedor de CNG assimétrico.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a></td>
<td>Aloca memória para um buffer. Essa memória é usada por todas as funções crypt32. lib que retornam buffers alocados.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>CryptMemFree</strong></a></td>
<td>Libera memória alocada por <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a> ou <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a></td>
<td>Libera a memória alocada atualmente para um buffer, e aloca memória para um novo buffer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Recupera informações sobre o conteúdo de um BLOB ou de um arquivo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>Codifica as informações a serem &quot; assinadas &quot; , assina essas informações codificadas e codifica as informações resultantes assinadas.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>CryptSignCertificate</strong></a></td>
<td>Assina as &quot; informações a serem assinadas &quot; no conteúdo codificado e assinado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a></td>
<td>Adiciona um pacote de interface de entidade (SIP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>CryptSIPCreateIndirectData</strong></a></td>
<td>Retorna uma estrutura de <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a> que contém um <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> da estrutura de <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a> fornecida, o algoritmo de resumo e um atributo de codificação. O hash pode ser usado como uma referência indireta aos dados.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>CryptSIPGetCaps</strong></a></td>
<td>Recupera os recursos de um SIP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>CryptSIPGetSignedDataMsg</strong></a></td>
<td>Recupera uma assinatura Authenticode do arquivo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>CryptSIPLoad</strong></a></td>
<td>Carrega a biblioteca de vínculo dinâmico que implementa um pacote de interface de entidade e atribui funções de exportação de biblioteca apropriadas a uma estrutura de <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>CryptSIPPutSignedDataMsg</strong></a></td>
<td>Armazena uma assinatura Authenticode no arquivo de destino.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>CryptSIPRemoveProvider</strong></a></td>
<td>Remove um SIP adicionado por uma chamada anterior à função <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>CryptSIPRemoveSignedDataMsg</strong></a></td>
<td>Remove uma assinatura Authenticode especificada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>CryptSIPRetrieveSubjectGuid</strong></a></td>
<td>Recupera um GUID com base nas informações de cabeçalho em um arquivo especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>CryptSIPRetrieveSubjectGuidForCatalogFile</strong></a></td>
<td>Recupera o GUID do assunto associado ao arquivo especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>CryptSIPVerifyIndirectData</strong></a></td>
<td>Valida os dados indiretos com hash no assunto fornecido.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>CryptUpdateProtectedState</strong></a></td>
<td>Migra as chaves mestras do usuário atual após a alteração do Sid ( <a href="/windows/desktop/SecGloss/s-gly"><em>identificador de segurança</em></a> ) do usuário.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a></td>
<td>Verifica a assinatura de um certificado de entidade ou uma <a href="/windows/desktop/SecGloss/c-gly"><em>CRL</em></a> usando as informações de chave pública.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>CryptVerifyCertificateSignatureEx</strong></a></td>
<td>Uma versão estendida do <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>GetEncSChannel</strong></a></td>
<td>Armazena o conteúdo da DLL Schannel criptografada na memória.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pCryptSIPGetCaps</strong></a></td>
<td>Implementado por um SIP para recursos de relatório.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Funções de conversão de dados

As funções CryptoAPI a seguir convertem membros da estrutura de certificado em formulários diferentes.

| Função                                           | Descrição                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAlgIdToOID**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Converte um identificador de algoritmo CryptoAPI ( \_ ID alg) em uma cadeia de caracteres de identificação de objeto (ASN. 1) de uma [*preobject*](../secgloss/o-gly.md) [*Notation*](../secgloss/a-gly.md) . |
| [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Adquire o assunto ou o nome do emissor de um certificado e o converte em uma cadeia de caracteres terminada em nulo.                                                                                                                                                                                                               |
| [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Converte um [*blob*](../secgloss/b-gly.md) de nome de certificado em uma cadeia de caracteres terminada em zero.                                                                                                                                                                                                      |
| [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Converte a cadeia de caracteres do identificador de objeto ASN. 1 no identificador do algoritmo CSP.                                                                                                                                                                                                                                                 |
| [**CertRDNValueToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Converte um valor de nome em uma cadeia de caracteres terminada em nulo.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Converte uma cadeia de caracteres [*X. 500*](../secgloss/x-gly.md) terminada em nulo em um nome de certificado codificado.                                                                                                                                                                                          |
| [**CryptBinaryToString**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Converte uma sequência binária em uma cadeia de caracteres formatada.                                                                                                                                                                                                                                                                          |
| [**CryptFormatObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Formata dados codificados e retorna uma cadeia de caracteres Unicode.                                                                                                                                                                                                                                                                          |
| [**CryptStringToBinary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Converte uma cadeia de caracteres formatada em uma sequência binária.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Funções de uso avançado de chave

As funções a seguir lidam com a extensão EKU ( [*uso avançado de chave*](../secgloss/e-gly.md) ) e a propriedade EKU estendida de certificados. A extensão EKU e a propriedade estendida especificam e limitam os usos válidos de um certificado. As extensões fazem parte do próprio certificado. Eles são definidos pelo emissor do certificado e são somente leitura. As propriedades estendidas de certificado são valores associados a um certificado que pode ser definido em um aplicativo.

| Função                                                                             | Descrição                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CertAddEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Adiciona um identificador de uso à propriedade EKU de um certificado.                       |
| [**CertGetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Adquire, de um certificado, informações sobre a extensão ou Propriedade EKU. |
| [**CertRemoveEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Remove o identificador de uso da propriedade estendida EKU de um certificado.       |
| [**CertSetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Define a propriedade EKU para um certificado.                                       |



 

### <a name="key-identifier-functions"></a>Funções de identificador de chave

As funções de identificador de chave permitem que o usuário crie, defina, recupere ou localize um identificador de chave ou suas propriedades.

Um identificador de chave é o identificador exclusivo de um [*par de chaves pública/privada*](../secgloss/p-gly.md). Pode ser qualquer identificador exclusivo, mas geralmente é o hash SHA1 de 20 bytes de uma estrutura [**de \_ \_ \_ informações de chave pública de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) codificado. Um identificador de chave pode ser obtido por meio da ID de prop do identificador de chave de certificado \_ \_ \_ \_ . O identificador de chave permite o uso desse [*par de chaves*](../secgloss/k-gly.md) para criptografar ou descriptografar mensagens sem usar o certificado.

Os identificadores de chave não estão associados a [*CRLs*](../secgloss/c-gly.md) ou [*CTLs*](../secgloss/c-gly.md).

Um identificador de chave pode ter as mesmas propriedades que um contexto de certificado. Para obter mais informações, consulte [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>CryptCreateKeyIdentifierFromCSP</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Cria um identificador de chave do BLOB de <a href="/windows/desktop/SecGloss/p-gly"><em>chave pública</em></a>de um CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>CryptEnumKeyIdentifierProperties</strong></a></td>
<td>Enumera os identificadores de chave e suas propriedades.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>CryptGetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Adquire uma propriedade específica de um identificador de chave especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>CryptSetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Essa API está preterida. O software novo e o existente devem começar a usar <a href="/windows/desktop/SecCNG/cng-portal">APIs de próxima geração de criptografia.</a> A Microsoft poderá remover essa API em versões futuras.
</blockquote>
<br/> Define uma propriedade de um identificador de chave especificado.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>Funções de suporte a OID

Essas funções fornecem suporte a OID ( [*identificador de objeto*](../secgloss/o-gly.md) ). Essas funções instalam, registram e expedem para OID e codificam funções específicas de tipo.

As seguintes funções de CryptoAPI usam essas funções de suporte a OID:

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Para obter uma visão geral desse processo, consulte [estendendo a funcionalidade de CryptoAPI](extending-cryptoapi-functionality.md).

As funções a seguir funcionam com OIDs.

| Função                                                                       | Descrição                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Enumera as funções de OID registradas identificadas por seu tipo de codificação, nome de função e OID.                                                                                                                 |
| [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Enumera as informações de OID registradas identificadas por seu grupo e chama *pfnEnumOIDInfo* para correspondências.                                                                                                       |
| [**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Usa a chave e o grupo especificados para localizar informações de OID.                                                                                                                                                          |
| [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Libera a contagem de identificadores que foi incrementada e retornada por [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) ou [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress). |
| [**CryptGetDefaultOIDDllList**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Adquire a lista de entradas de DLL padrão registradas para o conjunto de funções e o tipo de codificação especificados.                                                                                                              |
| [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Adquire a primeira ou próxima função padrão instalada ou carrega a DLL que contém a função padrão.                                                                                                 |
| [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Pesquisa a lista de funções instaladas para um tipo de codificação e uma correspondência de OID. Se uma correspondência não for encontrada, o registro será pesquisado em busca de uma correspondência.                                                                  |
| [**CryptGetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Adquire o valor para o tipo de codificação especificado, o nome da função, o OID e o nome do valor.                                                                                                                            |
| [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Inicializa e retorna um identificador do conjunto de funções de OID identificado pelo nome de função fornecido.                                                                                                                 |
| [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Instala um conjunto de endereços de função OID que podem ser chamados.                                                                                                                                                                 |
| [**CryptRegisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Registra a DLL que contém a função padrão a ser chamada para o tipo de codificação e o nome da função especificados.                                                                                               |
| [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Registra a DLL que contém a função a ser chamada para o tipo de codificação especificado, o nome da função e a OID.                                                                                                 |
| [**CryptRegisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Registra as informações de OID especificadas na estrutura de [**\_ \_ informações de OID cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) , mantendo-as para o registro.                                                                                |
| [**CryptSetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Define o valor para o tipo de codificação especificado, o nome da função, o OID e o nome do valor.                                                                                                                                |
| [**CryptUnregisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Remove o registro da DLL que contém a função padrão a ser chamada para o tipo de codificação e o nome da função especificados.                                                                            |
| [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Remove o registro da DLL que contém a função a ser chamada para o tipo de codificação especificado, o nome da função e o OID.                                                                              |
| [**CryptUnregisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Remove o registro das informações de OID especificadas.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Funções de recuperação de objeto remoto

As funções a seguir permitem que o usuário recupere um objeto PKI (infraestrutura de chave pública), adquira a URL de um certificado, CTL ou CRL, ou Extraia uma URL de um objeto.

| Função                                                     | Descrição                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**CryptGetObjectUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Adquire a URL do objeto remoto de um certificado, CTL ou CRL. |
| [**CryptRetrieveObjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Recupera o objeto PKI de um local especificado por uma URL.           |



 

### <a name="pfx-functions"></a>Funções PFX

As funções a seguir dão suporte a [*BLOBs*](../secgloss/b-gly.md)de formato PFX (troca de informações pessoais).

| Função                                             | Descrição                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFXExportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | As exportações do certificado referenciado [*Armazenam*](../secgloss/c-gly.md) os certificados e, se disponíveis, suas [*chaves privadas*](../secgloss/p-gly.md)associadas. |
| [**PFXExportCertStoreEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | As exportações do certificado referenciado armazenam os certificados e, se disponíveis, suas chaves privadas associadas.                                                                                                                                                             |
| [**PFXImportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Importa um BLOB PFX e retorna o identificador de um repositório que contém certificados e quaisquer chaves privadas associadas.                                                                                                                                                            |
| [**PFXIsPFXBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Tenta decodificar a camada externa de um BLOB como um pacote PFX.                                                                                                                                                                                                                |
| [**PFXVerifyPassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Tenta decodificar a camada externa de um BLOB como um pacote PFX e descriptografá-lo com a senha fornecida.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Funções de backup e restauração dos serviços de certificados

Os serviços de certificados incluem funções para fazer backup e restaurar o banco de dados de serviços de certificados. Essas funções de backup e restauração dos serviços de certificados estão contidas em Certadm.dll. Ao contrário dos outros elementos de API associados aos serviços de certificados, essas funções não são encapsuladas em um objeto que pode ser usado para chamar métodos de classe. Em vez disso, as APIs de backup e restauração são chamadas primeiro carregando a biblioteca de Certadm.dll na memória chamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e, em seguida, determinando o endereço das funções chamando [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Quando terminar de chamar as funções de backup e restauração dos serviços de certificados, chame o [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar recursos de Certadm.dll da memória.

> [!Note]
> As funções de backup e restauração fornecidas pelo Certadm.dll não fazem backup ou restauram as [*chaves privadas*](../secgloss/p-gly.md)do serviço de certificado. Para obter informações sobre como fazer backup das chaves privadas dos serviços de certificados, consulte [fazendo backup e restaurando a chave privada dos serviços de certificados](backing-up-and-restoring-the-certificate-services-private-key.md).
> 
> Para chamar as funções de backup e restauração, você deve ter [*privilégios*](../secgloss/p-gly.md)de backup e restauração. Para obter detalhes, consulte [definindo os privilégios de backup e restauração](setting-the-backup-and-restore-privileges.md).

 

> [!Note]  
> Se **CoInitializeEx** foi chamado anteriormente no mesmo thread usado para chamar as APIs de backup e restauração dos serviços de certificados, o \_ sinalizador APARTMENTTHREADED deve ter sido passado para **CoInitializeEx**. Ou seja, ao usar o mesmo thread, você não poderá chamar a API de backup e restauração dos serviços de certificados se o thread tiver passado anteriormente no sinalizador de multithread do coinit \_ em uma chamada de **CoInitializeEx**.

 

As APIs de backup dos serviços de certificados são definidas em Certbcli. h. No entanto, ao criar seu programa, use o certsrv. h como o arquivo de inclusão.

As APIs a seguir são exportadas por Certadm.dll.

| Função                                                                         | Descrição                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Fecha um arquivo aberto.                                                                                                |
| [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Finaliza uma sessão de backup.                                                                                                |
| [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Libera um buffer alocado pelas APIs de backup e restauração.                                                              |
| [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Retorna uma lista de arquivos de log que precisam ser submetidos a backup.                                                                |
| [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Retorna uma lista de arquivos de banco de dados que precisam ser copiados em backup.                                                           |
| [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Recupera a lista de nomes de arquivos dinâmicos de serviços de certificados que precisam de backup para o contexto de backup fornecido. |
| [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Abre um arquivo na preparação para fazer backup.                                                                        |
| [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Prepara o banco de dados para o backup online.                                                                          |
| [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Lê o conteúdo de um arquivo aberto.                                                                                 |
| [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Trunca os arquivos de log.                                                                                              |
| [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Determina se um servidor de serviços de certificados está online (executando ativamente).                                        |
| [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Finaliza uma sessão de restauração.                                                                                               |
| [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Recupera locais de banco de dados (usados para cenários de backup e restauração).                                            |
| [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Inicia uma sessão de restauração.                                                                                             |
| [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Registra uma operação de restauração.                                                                                        |
| [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Conclui uma operação de restauração registrada anteriormente.                                                                  |
| [**CertSrvRestoreRegisterThroughFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Registra uma operação de restauração.                                                                                        |
| [**CertSrvServerControl**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Envia um comando de controle para a instância de serviços de certificados.                                                         |



 

## <a name="callback-functions"></a>Funções de retorno de chamada

As funções de retorno de chamada nesta seção são usadas para registrar ou instalar provedores de [*repositório de certificados*](../secgloss/c-gly.md) definidos pelo aplicativo e para fornecer funcionalidade relacionada por meio de funções de retorno de chamada. As funções de retorno de chamada são implementadas por um aplicativo e são chamadas por funções de [*CryptoAPI*](../secgloss/c-gly.md) . As funções de retorno de chamada permitem que o aplicativo controle, em parte, a maneira como as funções de CryptoAPI manipulam dados.

| Função de retorno de chamada                                                                                                        | Uso                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertChainFindByIssuerCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Uma função de retorno de chamada definida pelo aplicativo que permite que o aplicativo filtre certificados que podem ser adicionados à cadeia de certificados.                                                                                                                                                                                                     |
| [**CertDllOpenStoreProv**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Define a função de abertura do provedor de repositório.                                                                                                                                                                                                                                                                                                     |
| [**CertEnumPhysicalStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Função de retorno de chamada usada pela função [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) para formatar e apresentar informações em cada repositório físico encontrado.                                                                                                                                                                                 |
| [**CertEnumSystemStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Função de retorno de chamada usada pela função [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) para formatar e apresentar informações em cada repositório físico encontrado.                                                                                                                                                                                     |
| [**CertEnumSystemStoreLocationCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Função de retorno de chamada usada pela função [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) para formatar e apresentar informações em cada repositório físico encontrado.                                                                                                                                                                     |
| [**CertStoreProvCloseCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Determina o que acontece quando a contagem de [*referência*](../secgloss/r-gly.md) de um repositório aberto se torna zero.                                                                                                                                                                                    |
| [**CertStoreProvControl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Permite que um aplicativo seja notificado quando há uma diferença entre o conteúdo de um armazenamento em cache em uso e o conteúdo desse repositório, pois ele é persistido no armazenamento.                                                                                                                                                                   |
| [**CertStoreProvDeleteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Determina as ações a serem tomadas antes de um certificado ser excluído de um repositório de certificados.                                                                                                                                                                                                                                                      |
| [**CertStoreProvDeleteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Determina as ações a serem tomadas antes que uma CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) seja excluída de um repositório de certificados.                                                                                                                        |
| [**CertStoreProvDeleteCTL**](certstoreprovdeletectl.md)                                                                 | Determina se uma CTL pode ser excluída.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvFindCert**](certstoreprovfindcert.md)                                                                   | Localiza o primeiro certificado, ou próximo, em um repositório que corresponda aos critérios especificados.                                                                                                                                                                                                                                                             |
| [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)                                                                     | Localiza a primeira ou próxima CRL em um repositório que corresponda aos critérios especificados.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFindCTL**](certstoreprovfindctl.md)                                                                     | Localiza o primeiro, ou próximo, CTL em um repositório que corresponda aos critérios especificados.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFreeFindCert**](certstoreprovfreefindcert.md)                                                           | Libera um contexto de certificado encontrado anteriormente.                                                                                                                                                                                                                                                                                                 |
| [**CertStoreProvFreeFindCRL**](certstoreprovfreefindcrl.md)                                                             | Libera um contexto de CRL encontrado anteriormente.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvFreeFindCTL**](certstoreprovfreefindctl.md)                                                             | Libera um contexto de CTL encontrado anteriormente.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvGetCertProperty**](certstoreprovgetcertproperty.md)                                                     | Recupera uma propriedade especificada de um certificado.                                                                                                                                                                                                                                                                                              |
| [**CertStoreProvGetCRLProperty**](certstoreprovgetcrlproperty.md)                                                       | Recupera uma propriedade especificada de uma CRL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvGetCTLProperty**](certstoreprovgetctlproperty.md)                                                       | Recupera uma propriedade especificada de uma CTL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Atualmente não usado, mas pode ser exportado para CSPs futuros.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Atualmente não usado, mas pode ser exportado para CSPs futuros.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCTL**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Leia a cópia do contexto de CTL do provedor e, se existir, crie um novo contexto de CTL.                                                                                                                                                                                                                                                     |
| [**CertStoreProvSetCertPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Determina as ações a serem tomadas antes de uma chamada para [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) ou [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty).                                                                                                                             |
| [**CertStoreProvSetCRLPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Determina as ações a serem tomadas antes de uma chamada para [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) ou [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty).                                                                                                                                                             |
| [**CertStoreProvSetCTLProperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Determina se uma propriedade pode ser definida em uma CTL.                                                                                                                                                                                                                                                                                            |
| [**CertStoreProvWriteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Determina as ações a serem tomadas antes de adicionar um certificado a um repositório.                                                                                                                                                                                                                                                                        |
| [**CertStoreProvWriteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Determina as ações a serem tomadas antes de adicionar uma CRL a um repositório.                                                                                                                                                                                                                                                                                |
| [**CertStoreProvWriteCTL**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Determina se uma CTL pode ser adicionada ao repositório.                                                                                                                                                                                                                                                                                           |
| [**\_ \_ prop keyid de enumeração de cript. \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Função de retorno de chamada usada pela função [**CryptEnumKeyIdentifierProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties) .                                                                                                                                                                                                                          |
| [**\_função de \_ OID de enumeração cript \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Função de retorno de chamada usada pela função [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction) .                                                                                                                                                                                                                                                  |
| [**\_informações de \_ OID de enumeração cript. \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Função de retorno de chamada usada pela função [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo) .                                                                                                                                                                                                                                                          |
| [**CryptGetSignerCertificateCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Função de retorno de chamada usada com a estrutura de [**\_ verificação de \_ mensagens \_ criptografadas**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) para obter e verificar o certificado de um signatário de mensagem.                                                                                                                                                                                 |
| [**PCRYPT \_ descriptografar \_ \_ chave privada \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Função de retorno de chamada usada pela função [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**PCRYPT \_ criptografar \_ \_ chave privada \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Função de retorno de chamada usada ao criar a estrutura de [**\_ \_ \_ \_ informações de chave privada criptografada cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info) .                                                                                                                                                                                                          |
| [**PCRYPT \_ resolver \_ HCRYPTPROV \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Função de retorno de chamada usada pela função [**CryptImportPKCS8**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8) .                                                                                                                                                                                                                                                          |
| [**\_retorno de \_ chamada de erro de análise \_ \_ do PFN CDF**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Uma função definida pelo usuário chamada para erros de função de definição de catálogo ao analisar um arquivo de definição de catálogo (CDF).                                                                                                                                                                                                                          |
| [**função \_ de \_ \_ classificação de contexto de criação \_ de certificado PFN \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Chamado para cada entrada de contexto classificada quando um contexto é criado.                                                                                                                                                                                                                                                                               |
| [**\_chave de \_ \_ criptografia de conteúdo de importação CNG \_ \_ PFN CMSG \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Uma função instalável do [*identificador de objeto*](../secgloss/o-gly.md) CNG (OID) para importação de uma CEK (chave de criptografia de conteúdo) já descriptografada.                                                                                                                                       |
| [**concordar com a \_ \_ \_ chave de importação CNG \_ do PFN CMSG \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Importa uma chave de criptografia de conteúdo para um destinatário de transporte de chave de uma mensagem envelopada.                                                                                                                                                                                                                                                       |
| [**\_Trans. \_ \_ chave de importação PFN CMSG CNG \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Uma função instalável de OID CNG para importação e [*descriptografia*](../secgloss/d-gly.md) de uma chave-transporte-destinatário, criptografada, CEK (chave de [*criptografia*](../secgloss/e-gly.md) de conteúdo).                                                                   |
| [**PFN \_ CMSG de \_ exportação de \_ chave \_ aceita**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Criptografa e exporta a chave de criptografia de conteúdo para um destinatário de contrato de chave de uma mensagem envelopada.                                                                                                                                                                                                                                        |
| [**\_trans de \_ chave de exportação PFN CMSG \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Criptografa e exporta a chave de criptografia de conteúdo para um destinatário de transporte de chave de uma mensagem envelopada.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ Exportar \_ lista de emails \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Criptografa e exporta a chave de criptografia de conteúdo para um destinatário de lista de endereçamento de uma mensagem envelopada.                                                                                                                                                                                                                                         |
| [**chave de criptografia de conteúdo do PFN \_ CMSG \_ Gen \_ \_ \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Gera a [*chave simétrica*](../secgloss/s-gly.md) usada para criptografar o conteúdo de uma mensagem envelopada.                                                                                                                                                                                     |
| [**PFN \_ CMSG de \_ importação de \_ chave \_ concorda**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Importa uma chave de criptografia de conteúdo para um destinatário de transporte de chave de uma mensagem envelopada.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ importar \_ chave \_ Trans**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Importa uma chave de criptografia de conteúdo para um destinatário de transporte de chave de uma mensagem envelopada.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ importar \_ lista de emails \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Importa uma chave de criptografia de conteúdo para um destinatário de transporte de chave de uma mensagem envelopada.                                                                                                                                                                                                                                                       |
| [**PFN \_ cript. \_ Exportar \_ informações de \_ chave pública \_ \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Chamado por [**CryptExportPublicKeyInfoEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) para exportar um blob de chave pública e codificá-lo.                                                                                                                                                                                                                         |
| [**PFN \_ cript. \_ extrair \_ parâmetros de assinatura codificados \_ \_ \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Chamado para decodificar e retornar o identificador do algoritmo de hash e, opcionalmente, os parâmetros de assinatura.                                                                                                                                                                                                                                            |
| [**PFN \_ cript \_ . \_ de \_ codificação e codifica \_ hash \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Chamado para assinar e codificar um hash calculado.                                                                                                                                                                                                                                                                                                    |
| [**PFN \_ criptu \_ verificar \_ assinatura codificada \_ \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Chamado para descriptografar uma assinatura codificada e compará-la a um hash calculado.                                                                                                                                                                                                                                                                     |
| [**PFN \_ importar \_ \_ informações de chave pública \_ \_ EX2 \_ Func**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Chamado por [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) para decodificar o identificador de [*algoritmo de chave pública*](../secgloss/p-gly.md) , carregar o provedor de algoritmo e importar o [*par de chaves*](../secgloss/k-gly.md). |
| [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)                                                                       | Uma função de retorno de chamada definida pelo usuário que permite que o chamador da função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) manipule a exibição de certificados que o usuário seleciona para exibir.                                                                                                                               |
| [**PFNCMFILTERPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Filtra cada certificado para decidir se ele aparecerá na caixa de diálogo seleção de certificado exibida pela função [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                |
| [**PFNCMHOOKPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Chamado antes que as mensagens sejam processadas pela caixa de diálogo seleção de certificado produzida pela função [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) .                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Funções de definição de catálogo

Essas funções são usadas para criar um catálogo. Todas essas funções são chamadas por [MakeCat](makecat.md).

| Função                                                                           | Descrição                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATCDFClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Fecha um arquivo de definição de catálogo e libera a memória para a estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) correspondente. |
| [**CryptCATCDFEnumAttributesWithCDFTag**](cryptcatcdfenumattributeswithcdftag.md) | Enumera os atributos dos arquivos de membro na seção **CatalogFiles** de um CDF.                                       |
| [**CryptCATCDFEnumCatAttributes**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Enumera os atributos de nível de catálogo na seção **CatalogHeader** de um CDF.                                        |
| [**CryptCATCDFEnumMembersByCDFTagEx**](cryptcatcdfenummembersbycdftagex.md)       | Enumera os membros do arquivo individual na seção **CatalogFiles** de um CDF.                                          |
| [**CryptCATCDFOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Abre um CDF existente para ler e Inicializa uma estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .                         |



 

## <a name="catalog-functions"></a>Funções de catálogo

Essas funções são usadas para gerenciar um catálogo.

| Função                                                                             | Descrição                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Adquire um identificador para um contexto de administrador de catálogo. Esse identificador pode ser usado por chamadas subsequentes para as funções [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog), [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)e [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) . |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Adquire um identificador para um contexto de administrador de catálogo para um determinado algoritmo de hash e política de hash.                                                                                                                                                                                                                                   |
| [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Adiciona um catálogo ao banco de dados de catálogo.                                                                                                                                                                                                                                                                                            |
| [**CryptCATAdminCalcHashFromFileHandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Calcula o hash de um arquivo.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Calcula o hash de um arquivo usando o algoritmo especificado.                                                                                                                                                                                                                                                                   |
| [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Enumera os catálogos que contêm um hash especificado.                                                                                                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCatalogContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Libera um identificador para um contexto de catálogo retornado anteriormente pela função [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog) .                                                                                                                                                                                             |
| [**CryptCATAdminReleaseContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Libera o identificador atribuído anteriormente pela função [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext) .                                                                                                                                                                                                        |
| [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | Exclui um arquivo de catálogo e remove a entrada do catálogo do banco de dados do catálogo do Windows.                                                                                                                                                                                                                                         |
| [**CryptCATAdminResolveCatalogPath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Recupera o caminho totalmente qualificado do catálogo especificado.                                                                                                                                                                                                                                                                       |
| [**CryptCATCatalogInfoFromContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Recupera informações de catálogo de um contexto de catálogo especificado.                                                                                                                                                                                                                                                                    |
| [**CryptCATClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Fecha um identificador de catálogo aberto anteriormente pela função [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) .                                                                                                                                                                                                                                    |
| [**CryptCATEnumerateAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Enumera os atributos associados a um membro de um catálogo.                                                                                                                                                                                                                                                                   |
| [**CryptCATEnumerateCatAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Enumera os atributos associados a um catálogo.                                                                                                                                                                                                                                                                               |
| [**CryptCATEnumerateMember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Enumera os membros de um catálogo.                                                                                                                                                                                                                                                                                               |
| [**CryptCATGetAttrInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Recupera informações sobre um atributo de um membro de um catálogo.                                                                                                                                                                                                                                                                 |
| [**CryptCATGetMemberInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Recupera informações de membro do PKCS 7 do catálogo \# . Além de recuperar as informações de membro para uma marca de referência especificada, essa função abre um contexto de membro.                                                                                                                                                    |
| [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Abre um catálogo e retorna um identificador de contexto para o catálogo aberto.                                                                                                                                                                                                                                                                 |
| [**Iscatalogfile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Recupera um valor booliano que indica se o arquivo especificado é um arquivo de catálogo.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>Funções WinTrust

As funções a seguir são usadas para executar várias operações de confiança.

| Função                                                                               | Descrição                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Adiciona uma ação de provedor de confiança ao sistema do usuário.                                                                                                                   |
| [**WintrustGetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Recupera os sinalizadores de política para um provedor de política.                                                                                                                        |
| [**WintrustAddDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Especifica o identificador de uso padrão e as informações de retorno de chamada para um provedor                                                                                       |
| [**WintrustGetDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Recupera o identificador de uso padrão e as informações de retorno de chamada.                                                                                                     |
| [**WintrustLoadFunctionPointers**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Carrega pontos de entrada de função para um GUID de ação especificado.                                                                                                             |
| [**WintrustRemoveActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Remove uma ação adicionada pela função [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid) .                                                                          |
| [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Define a configuração padrão que determina se os hashes de página são incluídos ao criar dados indiretos de SIP (pacote de interface de entidade) para arquivos executáveis portáteis. |
| [**WintrustSetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Define os sinalizadores de política para um provedor de política.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Executa uma ação de verificação de confiança em um objeto especificado.                                                                                                          |
| [**WinVerifyTrustEx**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Executa uma ação de verificação de confiança em um objeto especificado e usa um ponteiro para uma \_ estrutura de dados WINTRUST.                                                        |
| [**WTHelperCertCheckValidSignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Verifica se uma assinatura é válida.                                                                                                                                 |
| [**WTHelperCertFindIssuerCertificate**](wthelpercertfindissuercertificate.md)         | Localiza um certificado do emissor dos repositórios de certificados especificados que correspondem ao certificado de entidade especificado.                                                    |
| [**WTHelperCertIsSelfSigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Verifica se um certificado é autoassinado.                                                                                                                         |
| [**WTHelperGetFileHash**](wthelpergetfilehash.md)                                     | Verifica a assinatura de um arquivo assinado e Obtém o valor de hash e o identificador do algoritmo para o arquivo.                                                            |
| [**WTHelperGetProvCertFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Recupera um certificado de provedor de confiança da cadeia de certificados.                                                                                                   |
| [**WTHelperGetProvPrivateDataFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Recebe uma [**estrutura \_ \_ PRIVDATA do provedor cript**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) . da cadeia usando a ID do provedor.                                           |
| [**WTHelperGetProvSignerFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Recupera um signatário ou um subassinador por índice da cadeia.                                                                                                         |
| [**WTHelperProvDataFromStateData**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Recupera informações do provedor de confiança de um identificador especificado.                                                                                                        |



 

## <a name="object-locator-functions"></a>Funções do localizador de objeto

As seguintes funções de retorno de chamada podem ser implementadas por um provedor personalizado que deve ser chamado pelo pacote de segurança Schannel (canal seguro) para recuperar certificados.



| Função                                                                                                             | Descrição                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**\_liberação do \_ \_ provedor de localizador de objetos criptografados PFN \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Especifica que um objeto foi alterado.                   |
| [**\_Get do \_ \_ provedor de localizador de objeto PFN \_ cript \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Recupera um objeto.                                    |
| [**\_versão do \_ \_ provedor de localizador de objeto PFN \_ cript \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Libera o provedor.                                  |
| [**\_ \_ \_ \_ senha gratuita do provedor de localizador de objetos \_ PFN criptografado \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Libera a senha usada para criptografar uma matriz de bytes PFX. |
| [**\_provedor de \_ localizador de objetos criptografados PFN \_ \_ \_ gratuito**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Libera o objeto retornado pelo provedor.           |
| [**\_ \_ \_ \_ identificador gratuito do provedor de localizador de objetos \_ PFN criptografado \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Libera memória para um identificador de objeto.               |
| [**\_inicialização do \_ \_ provedor de localizador de objeto PFN \_ cript \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Inicializa o provedor.                               |



 

 

 
