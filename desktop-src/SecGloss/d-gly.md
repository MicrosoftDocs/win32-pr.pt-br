---
description: Contém definições de termos de segurança que começam com a letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d007cbb9-b547-4dc7-bc22-b526f650f7c2
title: D (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f81a17b2ba2c34b6d5367c1f920ad4b2a4048b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755033"
---
# <a name="d-security-glossary"></a>D (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_dac_gly"></span><span id="_SECURITY_DAC_GLY"></span>**DAC**
</dt> <dd>

Consulte *controle de acesso dinâmico*.

</dd> <dt>

<span id="_security_dacl_gly"></span><span id="_SECURITY_DACL_GLY"></span>**DACL**
</dt> <dd>

Consulte *lista de controle de acesso discricional*.

</dd> <dt>

<span id="_security_data_content_type_gly"></span><span id="_SECURITY_DATA_CONTENT_TYPE_GLY"></span>**tipo de conteúdo de dados**
</dt> <dd>

Um tipo de conteúdo base definido pelo PKCS \# 7. O conteúdo de dados é simplesmente uma cadeia de caracteres de octeto (Byte).

</dd> <dt>

<span id="_security_data_encryption_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_GLY"></span>**criptografia de dados**
</dt> <dd>

Consulte [*criptografia*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_function_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_FUNCTION_GLY"></span>**função de criptografia de dados**
</dt> <dd>

Consulte [*funções de criptografia e descriptografia*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_standard_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_STANDARD_GLY"></span>**Padrão de criptografia de dados**
</dt> <dd>

DES Uma codificação de bloco que criptografa dados em blocos de 64 bits. O DES é um algoritmo simétrico que usa o mesmo algoritmo e chave para criptografia e descriptografia.

Desenvolvido no início de 70, o DES também é conhecido como o DEA (algoritmo de criptografia de dados) por ANSI e o DEA-1 pela ISO.

</dd> <dt>

<span id="_security_datagram_gly"></span><span id="_SECURITY_DATAGRAM_GLY"></span>**datagrama**
</dt> <dd>

Um canal de comunicação que usa informações roteadas por meio de uma rede de troca de pacotes. Essas informações incluem pacotes separados de informações e as informações de entrega associadas a esses pacotes, como o endereço de destino. Em uma rede de comutação de pacotes, os pacotes de dados são roteados independentemente um do outro e podem seguir rotas diferentes. Eles também podem chegar em uma ordem diferente da que foi enviada.

</dd> <dt>

<span id="_security_decoding_gly"></span><span id="_SECURITY_DECODING_GLY"></span>**decodificação**
</dt> <dd>

O processo de converter um objeto codificado (como um certificado) ou dados de volta para seu formato original.

Em termos gerais, os dados são decodificados pela camada de codificação/decodificação do protocolo de comunicação. Os certificados são decodificados por uma chamada para a função **CryptDecodeObject** .

</dd> <dt>

<span id="_security_decryption_gly"></span><span id="_SECURITY_DECRYPTION_GLY"></span>**descriptografia**
</dt> <dd>

O processo de conversão de texto cifrado em texto não criptografado. A descriptografia é o oposto da criptografia.

</dd> <dt>

<span id="_security_default_mode_gly"></span><span id="_SECURITY_DEFAULT_MODE_GLY"></span>**modo padrão**
</dt> <dd>

Configurações padrão, como o modo de codificação de criptografia de bloco ou o método de preenchimento de criptografia de bloco.

</dd> <dt>

<span id="_security_der_gly"></span><span id="_SECURITY_DER_GLY"></span>**DER**
</dt> <dd>

Consulte *Distinguished Encoding Rules*.

</dd> <dt>

<span id="_security_derived_key_gly"></span><span id="_SECURITY_DERIVED_KEY_GLY"></span>**chave derivada**
</dt> <dd>

Uma chave de criptografia criada por uma chamada para a função **CryptDeriveKey** . Uma chave derivada pode ser criada com base em uma senha ou em qualquer outro dado de usuário. As chaves derivadas permitem que os aplicativos criem chaves de sessão conforme necessário, eliminando a necessidade de armazenar uma chave específica.

</dd> <dt>

<span id="_security_des_gly"></span><span id="_SECURITY_DES_GLY"></span>**DES**
</dt> <dd>

Consulte *padrão de criptografia de dados*.

</dd> <dt>

<span id="_security_dh_gly"></span><span id="_SECURITY_DH_GLY"></span>**FEITA**
</dt> <dd>

Consulte *algoritmo Diffie-Hellman*.

</dd> <dt>

<span id="_security_dh_keyx_gly"></span><span id="_SECURITY_DH_KEYX_GLY"></span>**DH \_ KEYX**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de troca de chave Diffie-Hellman.

Consulte também *algoritmo Diffie-Hellman*.

</dd> <dt>

<span id="_security_diffie_hellman_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_ALGORITHM_GLY"></span>**Algoritmo Diffie-Hellman**
</dt> <dd>

FEITA Um algoritmo de chave pública usado para proteger a troca de chaves. Diffie-Hellman não pode ser usado para criptografia de dados. Esse algoritmo é especificado como o algoritmo de troca de chaves \_ para \_ tipos de provedor DH do Prov DSS.

Consulte também *algoritmo de troca de chaves Diffie-Hellman (armazenar e encaminhar)* e o *algoritmo de troca de chave Diffie-Hellman (efêmero)*.

</dd> <dt>

<span id="_security_diffie_hellman_store_and_forward_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_STORE_AND_FORWARD_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Chave Diffie-Hellman (armazenamento e encaminhamento) – algoritmo de troca**
</dt> <dd>

Um algoritmo Diffie-Hellman em que os valores de chave do Exchange são retidos (no CSP) depois que o identificador de chave é destruído.

Consulte também *algoritmo de troca de chave Diffie-Hellman (efêmero)*.

</dd> <dt>

<span id="_security_diffie_hellman_ephemeral_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_EPHEMERAL_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Chave Diffie-Hellman (efêmera)-algoritmo de troca**
</dt> <dd>

Um algoritmo Diffie-Hellman em que o valor da chave do Exchange é excluído do CSP quando o identificador de chave é destruído.

Consulte também *algoritmo de troca de chaves Diffie-Hellman (armazenamento e encaminhamento)*.

</dd> <dt>

<span id="_security_digested_data_gly"></span><span id="_SECURITY_DIGESTED_DATA_GLY"></span>**dados resumidos**
</dt> <dd>

Um tipo de conteúdo de dados definido pelo PKCS \# 7 que consiste em qualquer tipo de dados, mais um hash de mensagem (Digest) do conteúdo.

</dd> <dt>

<span id="_security_digital_certificate_gly"></span><span id="_SECURITY_DIGITAL_CERTIFICATE_GLY"></span>**certificado digital**
</dt> <dd>

Consulte [*certificado*](c-gly.md).

</dd> <dt>

<span id="_security_digital_envelope_gly"></span><span id="_SECURITY_DIGITAL_ENVELOPE_GLY"></span>**envelope digital**
</dt> <dd>

Mensagens privadas criptografadas usando a chave pública do destinatário. As mensagens envelopadas só podem ser descriptografadas usando a chave privada do destinatário, permitindo que apenas o destinatário entenda a mensagem.

</dd> <dt>

<span id="_security_digital_signature_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_GLY"></span>**assinatura digital**
</dt> <dd>

Dados que associam a identidade de um remetente às informações que estão sendo enviadas. Uma assinatura digital pode ser agrupada com qualquer mensagem, arquivo ou outra informação codificada digitalmente ou transmitida separadamente. As assinaturas digitais são usadas em ambientes de chave pública e fornecem serviços de autenticação e integridade.

</dd> <dt>

<span id="_security_digital_signature_algorithm_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_ALGORITHM_GLY"></span>**Algoritmo de assinatura digital**
</dt> <dd>

DSA Um algoritmo de chave pública especificado pelo DSS (padrão de assinatura digital). O DSA é usado apenas para gerar assinaturas digitais. Ele não pode ser usado para criptografia de dados.

</dd> <dt>

<span id="_security_digital_signature_key_pair_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_KEY_PAIR_GLY"></span>**par de chaves de assinatura digital**
</dt> <dd>

Consulte [*par de chaves de assinatura*](s-gly.md).

</dd> <dt>

<span id="_security_digital_signature_standard_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_STANDARD_GLY"></span>**Padrão de assinatura digital**
</dt> <dd>

DSS Um padrão que especifica o algoritmo de assinatura digital (DSA) para seu algoritmo de assinatura e SHA-1 como seu algoritmo de hash de mensagem. DSA é uma codificação de chave pública que é usada somente para gerar assinaturas digitais e não pode ser usada para criptografia de dados. O DSS é especificado pelos \_ tipos de provedor Prov DSS, Prov \_ DSS \_ DH e Prov \_ Fortezza.

</dd> <dt>

<span id="_security_discretionary_access_control_list_gly"></span><span id="_SECURITY_DISCRETIONARY_ACCESS_CONTROL_LIST_GLY"></span>**lista de controle de acesso discricionário**
</dt> <dd>

DACL Uma lista de controle de acesso que é controlada pelo proprietário de um objeto e que especifica o acesso que usuários ou grupos específicos podem ter ao objeto.

Consulte também lista de [*controle de acesso*](a-gly.md) e lista de controle de [*acesso do sistema*](s-gly.md).

</dd> <dt>

<span id="_security_distinguished_encoding_rules_gly"></span><span id="_SECURITY_DISTINGUISHED_ENCODING_RULES_GLY"></span>**Distinguished Encoding Rules**
</dt> <dd>

DER Um conjunto de regras para codificar dados definidos por ASN. 1 como um fluxo de bits para armazenamento ou transmissão externa. Todo objeto ASN. 1 tem exatamente uma codificação DER correspondente. O DER é definido na recomendação de CCITT X. 509, seção 8,7. Esse é um dos dois métodos de codificação atualmente usados pelo CryptoAPI.

</dd> <dt>

<span id="_security_dll_gly"></span><span id="_SECURITY_DLL_GLY"></span>**DLL**
</dt> <dd>

Consulte *biblioteca de vínculo dinâmico*.

</dd> <dt>

<span id="_security_dsa_gly"></span><span id="_SECURITY_DSA_GLY"></span>**DSA**
</dt> <dd>

Consulte *algoritmo de assinatura digital*.

</dd> <dt>

<span id="_security_dss_gly"></span><span id="_SECURITY_DSS_GLY"></span>**DSS**
</dt> <dd>

Consulte *padrão de assinatura digital*.

</dd> <dt>

<span id="_security_dynamic_access_control_gly"></span><span id="_SECURITY_DYNAMIC_ACCESS_CONTROL_GLY"></span>**Controle de acesso dinâmico**
</dt> <dd>

DAC A capacidade de especificar políticas de controle de acesso com base em declarações de usuário, dispositivo e recurso. Isso torna a autenticação mais flexível para aplicativos enquanto mantém os requisitos de segurança e conformidade.

</dd> <dt>

<span id="_security_dynamic_link_library_gly"></span><span id="_SECURITY_DYNAMIC_LINK_LIBRARY_GLY"></span>**biblioteca de vínculo dinâmico**
</dt> <dd>

(DLL) um arquivo que contém rotinas executáveis que podem ser chamadas de outros aplicativos.

</dd> </dl>

 

 



