---
title: Propriedades do método EAP (Eaptypes. h)
description: Usado por suplicantes e autenticadores para determinar os métodos EAP a serem usados com um determinado suplicante ou autenticador. Propriedades do método também especificam a configuração de um método.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644736"
---
# <a name="eap-method-properties"></a>Propriedades do método EAP

Usado por suplicantes e autenticadores para determinar os métodos EAP a serem usados com um determinado suplicante ou autenticador. Propriedades do método também especificam a configuração de um método.

Por exemplo, o suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) pode exigir métodos para ter determinadas propriedades para uso com o suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) . O material de chaveamento, por exemplo, é um requisito.

As propriedades com suporte dos métodos EAP são listadas. As propriedades são armazenadas como valores de chave do registro. Para obter mais informações, consulte a seção chave do registro da DLL do método do par EAP do tópico [configuração do registro para métodos EAP.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



O método permite que o conjunto de codificação seja negociado para fins de criptografia de dados. O Windows Server 2008 dá suporte aos seguintes [conjuntos de codificação](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:

-   TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha (TLS & SSL 3)
-   TLS \_ DHE \_ DSS \_ com \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)
-   SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5 (SSL 2, se habilitado)

Para obter mais informações sobre o protocolo de segurança TLS 1,0, consulte [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



O método fornece uma troca, na qual o autenticador autentica o par e vice-versa.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



O método fornece autenticação de origem de dados e proteção contra modificação não autorizada de informações para pacotes EAP, incluindo solicitações e respostas de EAP. Ao fazer essa declaração, uma especificação de método deve especificar os pacotes EAP protegidos e os campos protegidos nos pacotes EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



O método pode proteger contra a repetição de um método EAP ou suas mensagens. As indicações de resultado de êxito e falha não podem ser reproduzidas.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



O método pode criptografar mensagens EAP. Solicitações EAP, respostas EAP, indicações de resultado de êxito e indicações de resultado de falha são criptografadas. Um método que faz essa declaração deve oferecer suporte à proteção de identidade.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



O método pode derivar material de chaveamento exportável, como a chave de sessão mestra (MSK) e a chave de sessão mestra estendida (EMSK). O MSK é usado apenas para maior derivação de chave, não diretamente para proteção da conversa EAP ou dados subsequentes. O uso de EMSK é reservado.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



O comprimento mínimo da chave com suporte pelo método EAP é de 64 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



O comprimento mínimo da chave com suporte pelo método EAP é de 128 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



O comprimento mínimo da chave com suporte pelo método EAP é de 256 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



O comprimento mínimo da chave com suporte pelo método EAP é de 512 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



O comprimento mínimo da chave com suporte pelo método EAP é de 1024 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



O método não permite um ataque offline com um fator de trabalho com base no número de senhas no dicionário de um invasor. Onde a autenticação de senha é usada, as senhas normalmente são selecionadas de um pequeno conjunto (em comparação com um conjunto de chaves de N bits), o que gera uma preocupação sobre ataques de dicionário. Um método pode ser considerado para fornecer proteção contra ataques de dicionário se, ao usar uma senha como um segredo, o método não permitir um ataque offline com um fator de trabalho baseado no número de senhas no dicionário de um invasor.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



O método tem a capacidade, no caso em que uma associação de segurança foi estabelecida anteriormente, para criar uma associação de segurança nova ou atualizada com mais eficiência ou em um número menor de viagens de ida e volta.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



O método demonstra ao servidor EAP que uma única entidade agiu como o par EAP para todos os métodos executados em um método de túnel. A associação também pode indicar que o servidor EAP demonstra ao par que uma única entidade agiu como o servidor EAP para todos os métodos executados em um método de túnel. Se executado corretamente, a ligação serve para atenuar as vulnerabilidades do Man-in-the-Middle.


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



O método demonstra que os ataques passivos (como captura da conversação EAP) ou ataques ativos (incluindo o comprometimento do MSK ou EMSK) não comprometem subseqüentes ou anteriores MSKs ou EMSKs.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



O método pode dar suporte à fragmentação e remontagem se os pacotes EAP excederem a MTU mínima (unidade de transmissão máxima) de 1020 octetos.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



O método pode comunicar Propriedades de canal protegidas por integridade, como identificadores de ponto de extremidade, que podem ser comparados a valores transmitidos usando mecanismos fora de banda, como uma [autenticação, autorização e contabilidade](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) ou o protocolo de camada inferior.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



O método dá suporte à NAP (proteção de acesso à rede).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



O método pode ser usado em um computador autônomo.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



O método dá suporte à criptografia [de protocolo MPPE (criptografia ponto a ponto) da Microsoft](https://go.microsoft.com/fwlink/p/?linkid=83915) .


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



O método dá suporte ao túnel de outros métodos EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



O método dá suporte a propriedades configuráveis e tem uma interface do usuário.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



O método foi certificado pelo programa de certificação EAP. Esse bit só deve ser enviado por métodos EAP que passaram na certificação.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 ou posterior: o método pode ser usado para autenticar um computador em uma rede usando as credenciais de computadores.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 ou posterior: o método pode ser usado para autenticar um usuário em uma rede usando as credenciais dos usuários.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 ou posterior: o método dá suporte ao envio da identidade do usuário em um canal protegido.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 ou posterior: o método é um método tunnelled e dá suporte ao encadeamento de métodos EAP no túnel.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 ou posterior: o método dá suporte à equivalência de estado compartilhado, conforme definido no [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Reservado. Não usado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Chaves do registro para métodos EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Constantes do EAPHost comuns](common-eap-host-error-constants.md)
</dt> </dl>

