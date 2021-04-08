---
description: Contém definições de termos de segurança que começam com a letra S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: S (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975df9e3638f12ba7f3766d6119685fba1fa599b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922106"
---
# <a name="s-security-glossary"></a>S (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) S [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

Consulte *Secure/Multipurpose Internet Mail Extensions*.

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**Right**
</dt> <dd>

Consulte *lista de controle de acesso do sistema*.

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**valor de Salt**
</dt> <dd>

Dados aleatórios que às vezes são incluídos como parte de uma chave de sessão. Quando adicionado a uma chave de sessão, os dados de texto sem formatação são colocados na frente dos dados de chave criptografados. Valores de Salt são adicionados para aumentar o trabalho necessário para montar um ataque de força bruta (dicionário) contra dados criptografados com uma codificação de chave simétrica. Os valores de Salt são gerados chamando **CryptGenRandom**.

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**Samuel**
</dt> <dd>

Consulte *Gerenciador de contas de segurança*.

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**nome corrigido**
</dt> <dd>

A forma de um nome de autoridade de certificação (CA) que é usado em nomes de arquivos (como para uma [*lista de certificados revogados*](c-gly.md)) e em chaves do registro. O processo de limpeza do nome da autoridade de certificação é necessário para remover os caracteres ilegais para nomes de arquivo, nomes de chave do registro ou valores de nome distintos, ou que são inválidos para motivos específicos da tecnologia. Nos serviços de certificados, o processo de limpeza converte qualquer caractere ilegal no nome comum da autoridade de certificação em uma representação de cinco caracteres no formato **!** _xxxx_, onde **!** é usado como um caractere de escape e *xxxx* representa quatro inteiros hexadecimais que identificam exclusivamente o caractere que está sendo convertido.

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**RÍGIDO**
</dt> <dd>

Consulte *sequência de atenção segura*.

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**Scartar $ defaultreadrs**
</dt> <dd>

No entanto, um grupo de leitores de terminal que contém todos os leitores atribuídos a esse terminal não está reservado para esse uso específico.

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**Scartar $ webreaders**
</dt> <dd>

Um grupo de leitores de todo o sistema de cartão inteligente que inclui todos os leitores introduzidos no Gerenciador de recursos de cartão inteligente. Os leitores são adicionados automaticamente ao grupo quando são introduzidos no sistema.

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**\_AUTOalocar scartar**
</dt> <dd>

Uma constante de sistema de cartão inteligente que diz ao Gerenciador de recursos de cartão inteligente para alocar memória suficiente, retornando um ponteiro para o buffer alocado em vez de preencher um buffer fornecido pelo usuário. O buffer retornado deve, eventualmente, ser liberado chamando **SCardFreeMemory**.

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

Consulte *protocolo SCEP*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**Schannel**
</dt> <dd>

Um pacote de segurança que fornece autenticação entre clientes e servidores.

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**sequência de atenção segura**
</dt> <dd>

RÍGIDO Uma sequência de chave que inicia o processo de logon ou desativação. A sequência padrão é CTRL + ALT + DEL.

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**Transação eletrônica segura**
</dt> <dd>

Definição Um protocolo para transações eletrônicas seguras pela Internet.

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**Algoritmo de hash seguro**
</dt> <dd>

Sha Um algoritmo de hash que gera um resumo de mensagem. O SHA é usado com o algoritmo de assinatura digital (DSA) no padrão de assinatura digital (DSS), entre outros locais. O CryptoAPI faz referência a esse algoritmo pelo identificador do algoritmo (CALG \_ SHA), pelo nome (SHA) e pela classe (alg \_ hash de classe \_ ). Há quatro variedades de SHA: SHA-1, SHA-256, SHA-384 e SHA-512. O SHA-1 gera um resumo de mensagens de 160 bits. SHA-256, SHA-384 e SHA-512 geram resumos de mensagens de 256 bits, de 384 bits e de 512 bits, respectivamente. O SHA foi desenvolvido pelo National Institute of Standards and Technology (NIST) e pela NSA (National Security Agency).

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**Hash seguro padrão**
</dt> <dd>

Um padrão projetado pelo NIST e pela NSA. Esse padrão define o algoritmo de hash seguro (SHA-1) para uso com o padrão de assinatura digital (DSS).

Consulte também *algoritmo de hash seguro*.

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**Protocolo protocolo SSL**
</dt> <dd>

SSL Um protocolo para comunicações de rede seguras usando uma combinação de tecnologia de chave pública e secreta.

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**Secure/Multipurpose Internet Mail Extensions**
</dt> <dd>

(S/MIME) Um padrão de segurança de email que usa criptografia de chave pública.

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**Gerente de contas de segurança**
</dt> <dd>

Samuel Um serviço do Windows usado durante o processo de logon. O SAM mantém as informações da conta de usuário, incluindo os grupos aos quais um usuário pertence.

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**contexto de segurança**
</dt> <dd>

Os atributos de segurança ou as regras que estão em vigor no momento. Por exemplo, o usuário atual fez logon no computador ou o número de identificação pessoal inserido pelo usuário do cartão inteligente. Para SSPI, um contexto de segurança é uma estrutura de dados opaca que contém dados de segurança relevantes para uma conexão, como uma chave de sessão ou uma indicação da duração da sessão.

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**descritor de segurança**
</dt> <dd>

Uma estrutura e dados associados que contêm as informações de segurança para um objeto protegível. Um descritor de segurança identifica o proprietário do objeto e o grupo primário. Ele também pode conter uma DACL que controla o acesso ao objeto e uma SACL que controla o log de tentativas de acessar o objeto.

Confira também [*descritor de segurança absoluto*](a-gly.md), [*lista de controle de acesso discricionário*](d-gly.md), *descritor de segurança auto-relativo*, *lista de controle de acesso do sistema*.

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**identificador de segurança**
</dt> <dd>

SIDs Uma estrutura de dados de comprimento variável que identifica contas de usuário, grupo e computador. Cada conta em uma rede recebe um SID exclusivo quando a conta é criada pela primeira vez. Os processos internos no Windows referem-se ao SID de uma conta em vez do nome do usuário ou do grupo da conta.

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**pacote de segurança**
</dt> <dd>

A implementação de software de um protocolo de segurança. Os pacotes de segurança estão contidos em DLLs do provedor de suporte de segurança ou no provedor de suporte de segurança/DLLs do pacote de autenticação.

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**Protocolo de segurança**
</dt> <dd>

Uma especificação que define objetos de dados relacionados à segurança e regras sobre como os objetos são usados para manter a segurança em um sistema de computador.

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**entidade de segurança**
</dt> <dd>

Uma entidade reconhecida pelo sistema de segurança. As entidades podem incluir usuários humanos, bem como processos autônomos.

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**provedor de suporte de segurança**
</dt> <dd>

SSP Uma DLL (biblioteca de vínculo dinâmico) que implementa o SSPI, disponibilizando um ou mais pacotes de segurança para os aplicativos. Cada pacote de segurança fornece mapeamentos entre as chamadas de função SSPI de um aplicativo e as funções de um modelo de segurança real. Os pacotes de segurança dão suporte a protocolos de segurança como a autenticação Kerberos e o Microsoft LAN Manager.

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**Interface do provedor de suporte de segurança**
</dt> <dd>

SSPI Uma interface comum entre aplicativos de nível de transporte, como a RPC (chamada de procedimento remoto) da Microsoft e provedores de segurança, como a segurança distribuída do Windows. O SSPI permite que um aplicativo de transporte chame um de vários provedores de segurança para obter uma conexão autenticada. Essas chamadas não exigem conhecimento extensivo dos detalhes do protocolo de segurança.

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**descritor de segurança auto-relativo**
</dt> <dd>

Um descritor de segurança que armazena todas as suas informações de segurança em um bloco contíguo de memória.

Consulte também *descritor de segurança*.

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**XmlSerializer**
</dt> <dd>

O processo de converter dados em uma cadeia de caracteres e zeros para que eles possam ser transmitidos em série. A codificação faz parte desse processo.

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**Formato do repositório de certificados serializado**
</dt> <dd>

SST O formato do repositório de certificados serializado é o único formato que preserva todas as propriedades do repositório de certificados. Isso é útil em casos como quando as raízes foram configuradas com propriedades EKU personalizadas e você deseja movê-las para outro computador.

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**servidor**
</dt> <dd>

Um computador que responde a comandos de um computador cliente. O cliente e o servidor trabalham juntos para executar a funcionalidade do aplicativo distributivo.

Consulte também [*cliente*](c-gly.md).

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**certificado do servidor**
</dt> <dd>

Refere-se a um certificado usado para autenticação de servidor, como autenticar um servidor Web em um navegador da Web. Quando um cliente de navegador da Web tenta acessar um servidor Web seguro, o servidor envia seu certificado ao navegador para permitir que ele verifique a identidade do servidor.

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**criptografia de entrada de servidor**
</dt> <dd>

SGC Uma extensão de *protocolo SSL* (SSL) que permite às organizações, como instituições financeiras, que têm versões de exportação do serviços de informações da Internet (IIS) para usar criptografia forte (por exemplo, criptografia de 128 bits).

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**nome da entidade de serviço**
</dt> <dd>

SPNs O nome pelo qual um cliente identifica exclusivamente uma instância de um serviço. Se você instalar várias instâncias de um serviço em computadores em uma floresta, cada instância deverá ter seu próprio SPN. Uma determinada instância de serviço pode ter vários SPNs se houver vários nomes que os clientes podem usar para autenticação

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**provedor de serviços (cartão inteligente)**
</dt> <dd>

Um componente de subsistema de cartão inteligente que fornece acesso a serviços de cartão inteligente específicos por meio de interfaces COM.

Consulte também [*provedor de serviços primário*](p-gly.md).

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**sessão**
</dt> <dd>

Uma troca de mensagens sob a proteção de uma única peça do material de chaveamento. Por exemplo, as sessões SSL usam uma única chave para enviar várias mensagens por essa chave.

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**chave de sessão**
</dt> <dd>

Uma chave de criptografia relativamente de curta duração, geralmente negociada por um cliente e um servidor com base em um segredo compartilhado. O ciclo de vida de uma chave de sessão é limitado pela sessão à qual ela está associada. Uma chave de sessão deve ser forte o suficiente para resistir a cryptanalysis durante o ciclo de vida da sessão. Quando as chaves de sessão são transmitidas, elas geralmente são protegidas com chaves de troca de chaves (que geralmente são chaves assimétricas) para que somente o destinatário pretendido possa acessá-las. As chaves de sessão podem ser derivadas de valores de hash chamando a função **CryptDeriveKey** .

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**esquema de derivação de chave de sessão**
</dt> <dd>

Especifica quando uma chave é derivada de um hash. Os métodos usados dependem do tipo de CSP.

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**Definição**
</dt> <dd>

Confira *transação eletrônica segura*.

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**SHA**
</dt> <dd>

O nome do CryptoAPI para o algoritmo de hash seguro, SHA-1. Outros algoritmos de hash incluem [*MD2*](m-gly.md), [*MD4*](m-gly.md)e [*MD5*](m-gly.md).

Consulte também *algoritmo de hash seguro*.

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**SHS**
</dt> <dd>

Consulte *padrão de hash seguro*.

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**SIDs**
</dt> <dd>

Consulte *identificador de segurança*.

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**funções de verificação de dados e assinatura**
</dt> <dd>

Funções de mensagens simplificadas usadas para assinar mensagens de saída e verificar a autenticidade de assinaturas aplicadas em mensagens recebidas e dados relacionados.

Consulte *funções de mensagens simplificadas*.

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**certificado de assinatura**
</dt> <dd>

Um certificado que contém uma chave pública que é usada para verificar assinaturas digitais.

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**arquivo de assinatura**
</dt> <dd>

Um arquivo que contém a assinatura de um CSP ( [*provedor de serviços de criptografia*](c-gly.md) ) específico. O arquivo de assinatura é necessário para garantir que o CryptoAPI reconheça o CSP. O CryptoAPI valida essa assinatura periodicamente para garantir que o CSP não tenha sido violado.

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**funções de assinatura**
</dt> <dd>

Funções usadas para criar e verificar assinaturas digitais.

Consulte também *funções de mensagens simplificadas*.

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**par de chaves de assinatura**
</dt> <dd>

O par de chaves pública/privada usado para autenticar mensagens (assinatura digital). Os pares de chave de assinatura são criados chamando **CryptGenKey**.

Consulte também [*par de chaves do Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**chave privada da assinatura**
</dt> <dd>

A chave privada de um par de chaves de assinatura.

Consulte *par de chaves de assinatura*.

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**dados assinados e envelopado**
</dt> <dd>

Um tipo de conteúdo de dados definido pelo PKCS \# 7. Esse tipo de dados consiste em conteúdo criptografado de qualquer tipo, chaves de criptografia de conteúdo criptografado para um ou mais destinatários e hashes de mensagens criptografadas duplicadas para um ou mais assinantes. A criptografia dupla consiste em uma criptografia com a chave privada de um signatário seguida por uma criptografia com a chave de criptografia de conteúdo.

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**dados assinados**
</dt> <dd>

Um tipo de conteúdo de dados definido pelo PKCS \# 7. Esse tipo de dados consiste em qualquer tipo de conteúdo além de hashes de mensagens criptografadas (resumos) do conteúdo para zero ou mais assinantes. Os hashes resultantes podem ser usados para confirmar quem assinou a mensagem. Esses hashes também confirmam que a mensagem original não foi modificada desde que a mensagem foi assinada.

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**protocolo SCEP**
</dt> <dd>

SCEP Um acrônimo que significa protocolo SCEP. Atualmente, o protocolo é um padrão de Internet de rascunho que define a comunicação entre os dispositivos de rede e uma autoridade de registro (RA) para registro de certificado. Para obter mais informações, consulte [o White Paper de implementação do Microsoft SCEP](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper).

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**BLOB de chave simples**
</dt> <dd>

Uma chave de sessão criptografada com a chave pública de troca de chaves do usuário de destino. Esse tipo de BLOB de chave é usado ao armazenar uma chave de sessão ou transmitir uma chave de sessão para outro usuário. Um BLOB de chave é criado chamando **CryptExportKey**.

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**funções de mensagens simplificadas**
</dt> <dd>

Funções de gerenciamento de mensagens, tais como criptografia de mensagens, descriptografia, assinatura e funções de verificação de assinatura. As funções de mensagens simplificadas operam em um nível mais alto do que as funções criptográficas base ou as funções de mensagens de nível baixo. As funções de mensagens simplificadas encapsulam várias das funções de criptografia base, de baixo nível e de certificado em uma única função que executa uma tarefa específica de uma maneira específica, como a criptografia de uma \# mensagem PKCS 7 ou a assinatura de uma mensagem.

Veja também [*funções de mensagens de nível baixo*](l-gly.md).

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**logon único**
</dt> <dd>

EXTERNO A capacidade de vincular um conta Microsoft (como uma conta do Microsoft Outlook.com) a uma conta local para que um logon permita que o usuário use outros aplicativos que dão suporte à entrada com seus conta Microsoft.

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**SIP**
</dt> <dd>

Consulte *pacote de interface do assunto*.

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**certificado do site**
</dt> <dd>

Os certificados de servidor e os certificados de [*autoridade de certificação*](c-gly.md) (CA) são chamados de certificados de site. Ao fazer referência a um certificado de servidor, o certificado identifica o servidor Web que está apresentando o certificado. Ao fazer referência a um certificado de autoridade de certificação, o certificado identifica a autoridade de certificação que emite certificados de autenticação de servidor e/ou cliente para os servidores e clientes que solicitam esses certificados.

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Skipjack**
</dt> <dd>

Um algoritmo de criptografia especificado como parte do pacote de criptografia Fortezza. Skipjack é uma codificação simétrica com um comprimento de chave fixo de 80 bits. Skipjack é um algoritmo classificado criado pelo Estados Unidos NSA (National Security Agency). Os detalhes técnicos do algoritmo Skipjack são secretos.

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**cartão inteligente**
</dt> <dd>

Um ICC (placa de circuito integrado) de propriedade de um indivíduo ou grupo cujas informações devem ser protegidas de acordo com as atribuições de propriedade específicas. Ele fornece seu próprio controle de acesso físico; sem o subsistema de cartão inteligente colocar o controle de acesso adicional no cartão inteligente. Um cartão inteligente é um cartão plástico que contém um circuito integrado compatível com ISO 7816.

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**caixa de diálogo comum de cartão inteligente**
</dt> <dd>

Uma caixa de diálogo comum que ajuda o usuário a selecionar e localizar um cartão inteligente. Ele funciona com os serviços de gerenciamento de banco de dados de cartão inteligente e os serviços de leitor para ajudar o aplicativo e, se necessário, o usuário, para identificar qual cartão inteligente usar para uma determinada finalidade.

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**banco de dados de cartão inteligente**
</dt> <dd>

O banco de dados usado pelo Gerenciador de recursos para gerenciar recursos. Ele contém uma lista de cartões inteligentes conhecidos, as interfaces e o provedor de serviços primário de cada cartão e leitores de cartão inteligente conhecidos e grupos de leitores.

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**subsistema de cartão inteligente**
</dt> <dd>

O subsistema usado para fornecer um link entre leitores de cartão inteligente e aplicativos com reconhecimento de cartão inteligente.

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**Certificado do fornecedor de software**
</dt> <dd>

SPC Um \# objeto de dados assinado PKCS 7 que contém certificados X. 509.

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**SPC**
</dt> <dd>

Consulte *certificado do fornecedor de software*.

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**SPNs**
</dt> <dd>

Consulte o *nome da entidade de serviço*.

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**SSL**
</dt> <dd>

Consulte *protocolo SSL protocolo*.

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**Algoritmo de autenticação de cliente SSL3**
</dt> <dd>

Um algoritmo usado para autenticação de cliente no protocolo SSL (SSL) versão 3. No protocolo SSL3, uma concatenação de um hash MD5 e de um hash SHA-1 é assinada com uma chave privada RSA. O CryptoAPI e o Microsoft base e os provedores criptográficos aprimorados dão suporte a SSL3 com o tipo de hash CALG \_ SSL3 \_ SHAMD5.

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**Protocolo SSL3**
</dt> <dd>

Versão 3 do protocolo protocolo SSL (SSL).

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**EXTERNO**
</dt> <dd>

Consulte *logon único*.

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**SSP**
</dt> <dd>

Consulte *provedor de suporte de segurança*.

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**SSPI**
</dt> <dd>

Consulte *interface do provedor de suporte de segurança*.

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**SST**
</dt> <dd>

Consulte *formato do repositório de certificados serializado*.

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**status**
</dt> <dd>

O conjunto de todos os valores persistentes associados a uma entidade criptográfica, como uma chave ou um hash. Esse conjunto pode incluir coisas como o [*vetor de inicialização*](i-gly.md) (IV) que está sendo usado, o algoritmo que está sendo usado ou o valor da entidade já calculada.

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**codificação de fluxo**
</dt> <dd>

Uma codificação que criptografa dados em série, um bit por vez.

Confira também [*Bloquear codificação*](b-gly.md).

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**pacote de subautenticação**
</dt> <dd>

Uma DLL opcional que fornece funcionalidade de autenticação adicional, normalmente estendendo o algoritmo de autenticação. Se um pacote de subautenticação estiver instalado, o pacote de autenticação chamará o pacote de subautenticação antes de retornar seu resultado de autenticação para a autoridade de segurança local (LSA).

Consulte também [*autoridade de segurança local*](l-gly.md).

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**pacote de interface do assunto**
</dt> <dd>

SIP Uma especificação proprietária da Microsoft para uma camada de software que permite que os aplicativos criem, armazenem, recuperem e verifiquem uma assinatura de assunto. Os assuntos incluem, mas não se limitam a, imagens executáveis portáteis (. exe), imagens de gabinete (. cab), arquivos simples e arquivos de catálogo. Cada tipo de entidade usa um subconjunto diferente de seus dados para o cálculo de hash e requer um procedimento diferente para armazenamento e recuperação. Portanto, cada tipo de assunto tem uma especificação de pacote de interface de entidade exclusiva.

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

Um conjunto de algoritmos de criptografia declarado de forma aberta pela Agência de segurança nacional dos EUA como parte de seu programa de modernização de criptografia.

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**credenciais complementares**
</dt> <dd>

Credenciais para uso na autenticação de uma *entidade de segurança* para domínios de segurança externa.

Consulte também [*credenciais primárias*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**algoritmo simétrico**
</dt> <dd>

Um algoritmo criptográfico que normalmente usa uma única chave, geralmente conhecida como chave de sessão, para criptografia e descriptografia. Os algoritmos simétricos podem ser divididos em duas categorias, algoritmos de fluxo e algoritmos de bloco (também chamados de *fluxo* e [*codificações de bloco*](b-gly.md)).

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**criptografia simétrica**
</dt> <dd>

Criptografia que usa uma chave única para criptografia e descriptografia. A criptografia simétrica é preferida ao criptografar grandes quantidades de dados. Alguns dos algoritmos de criptografia simétrica mais comuns são [*RC2*](r-gly.md), [*RC4*](r-gly.md)e des ( [*Data Encryption Standard*](d-gly.md) ).

Consulte também [*criptografia de chave pública*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**chave simétrica**
</dt> <dd>

Uma chave secreta usada com um algoritmo de criptografia simétrica (ou seja, um algoritmo que usa a mesma chave para criptografia e descriptografia). Essa chave deve ser conhecida por todas as partes que se comunicam.

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**lista de controle de acesso do sistema**
</dt> <dd>

Right Uma ACL que controla a geração de mensagens de auditoria para tentativas de acessar um objeto protegível. A capacidade de obter ou definir a SACL de um objeto é controlada por um privilégio normalmente mantido apenas pelos administradores do sistema.

Consulte também [*lista de controle de acesso*](a-gly.md), [*lista de controle de acesso condicional*](d-gly.md), [*privilégio*](p-gly.md).

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**interface de programa do sistema**
</dt> <dd>

O conjunto de funções fornecido por um CSP ( [*provedor de serviços de criptografia*](c-gly.md) ) que implementa as funções de um aplicativo.

</dd> </dl>

 

 



