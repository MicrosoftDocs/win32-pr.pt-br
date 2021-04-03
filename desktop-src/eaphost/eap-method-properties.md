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
# <a name="eap-method-properties"></a><span data-ttu-id="f256f-104">Propriedades do método EAP</span><span class="sxs-lookup"><span data-stu-id="f256f-104">EAP Method Properties</span></span>

<span data-ttu-id="f256f-105">Usado por suplicantes e autenticadores para determinar os métodos EAP a serem usados com um determinado suplicante ou autenticador.</span><span class="sxs-lookup"><span data-stu-id="f256f-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="f256f-106">Propriedades do método também especificam a configuração de um método.</span><span class="sxs-lookup"><span data-stu-id="f256f-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="f256f-107">Por exemplo, o suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) pode exigir métodos para ter determinadas propriedades para uso com o suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f256f-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="f256f-108">O material de chaveamento, por exemplo, é um requisito.</span><span class="sxs-lookup"><span data-stu-id="f256f-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="f256f-109">As propriedades com suporte dos métodos EAP são listadas.</span><span class="sxs-lookup"><span data-stu-id="f256f-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="f256f-110">As propriedades são armazenadas como valores de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="f256f-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="f256f-111">Para obter mais informações, consulte a seção chave do registro da DLL do método do par EAP do tópico [configuração do registro para métodos EAP.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="f256f-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="f256f-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span><span class="sxs-lookup"><span data-stu-id="f256f-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f256f-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f256f-114">O método permite que o conjunto de codificação seja negociado para fins de criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="f256f-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="f256f-115">O Windows Server 2008 dá suporte aos seguintes [conjuntos de codificação](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:</span><span class="sxs-lookup"><span data-stu-id="f256f-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="f256f-116">TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="f256f-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="f256f-117">TLS \_ DHE \_ DSS \_ com \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="f256f-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="f256f-118">SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5 (SSL 2, se habilitado)</span><span class="sxs-lookup"><span data-stu-id="f256f-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="f256f-119">Para obter mais informações sobre o protocolo de segurança TLS 1,0, consulte [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="f256f-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span><span class="sxs-lookup"><span data-stu-id="f256f-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f256f-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="f256f-122">O método fornece uma troca, na qual o autenticador autentica o par e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="f256f-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span><span class="sxs-lookup"><span data-stu-id="f256f-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f256f-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="f256f-125">O método fornece autenticação de origem de dados e proteção contra modificação não autorizada de informações para pacotes EAP, incluindo solicitações e respostas de EAP.</span><span class="sxs-lookup"><span data-stu-id="f256f-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="f256f-126">Ao fazer essa declaração, uma especificação de método deve especificar os pacotes EAP protegidos e os campos protegidos nos pacotes EAP.</span><span class="sxs-lookup"><span data-stu-id="f256f-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span><span class="sxs-lookup"><span data-stu-id="f256f-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f256f-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="f256f-129">O método pode proteger contra a repetição de um método EAP ou suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="f256f-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="f256f-130">As indicações de resultado de êxito e falha não podem ser reproduzidas.</span><span class="sxs-lookup"><span data-stu-id="f256f-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span><span class="sxs-lookup"><span data-stu-id="f256f-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f256f-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="f256f-133">O método pode criptografar mensagens EAP.</span><span class="sxs-lookup"><span data-stu-id="f256f-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="f256f-134">Solicitações EAP, respostas EAP, indicações de resultado de êxito e indicações de resultado de falha são criptografadas.</span><span class="sxs-lookup"><span data-stu-id="f256f-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="f256f-135">Um método que faz essa declaração deve oferecer suporte à proteção de identidade.</span><span class="sxs-lookup"><span data-stu-id="f256f-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="f256f-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f256f-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="f256f-138">O método pode derivar material de chaveamento exportável, como a chave de sessão mestra (MSK) e a chave de sessão mestra estendida (EMSK).</span><span class="sxs-lookup"><span data-stu-id="f256f-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="f256f-139">O MSK é usado apenas para maior derivação de chave, não diretamente para proteção da conversa EAP ou dados subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f256f-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="f256f-140">O uso de EMSK é reservado.</span><span class="sxs-lookup"><span data-stu-id="f256f-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="f256f-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="f256f-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="f256f-143">O comprimento mínimo da chave com suporte pelo método EAP é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f256f-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="f256f-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f256f-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="f256f-146">O comprimento mínimo da chave com suporte pelo método EAP é de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="f256f-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="f256f-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="f256f-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="f256f-149">O comprimento mínimo da chave com suporte pelo método EAP é de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="f256f-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="f256f-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="f256f-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="f256f-152">O comprimento mínimo da chave com suporte pelo método EAP é de 512 bits.</span><span class="sxs-lookup"><span data-stu-id="f256f-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="f256f-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="f256f-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="f256f-155">O comprimento mínimo da chave com suporte pelo método EAP é de 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="f256f-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span><span class="sxs-lookup"><span data-stu-id="f256f-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="f256f-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="f256f-158">O método não permite um ataque offline com um fator de trabalho com base no número de senhas no dicionário de um invasor.</span><span class="sxs-lookup"><span data-stu-id="f256f-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="f256f-159">Onde a autenticação de senha é usada, as senhas normalmente são selecionadas de um pequeno conjunto (em comparação com um conjunto de chaves de N bits), o que gera uma preocupação sobre ataques de dicionário.</span><span class="sxs-lookup"><span data-stu-id="f256f-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="f256f-160">Um método pode ser considerado para fornecer proteção contra ataques de dicionário se, ao usar uma senha como um segredo, o método não permitir um ataque offline com um fator de trabalho baseado no número de senhas no dicionário de um invasor.</span><span class="sxs-lookup"><span data-stu-id="f256f-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span><span class="sxs-lookup"><span data-stu-id="f256f-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="f256f-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-163">O método tem a capacidade, no caso em que uma associação de segurança foi estabelecida anteriormente, para criar uma associação de segurança nova ou atualizada com mais eficiência ou em um número menor de viagens de ida e volta.</span><span class="sxs-lookup"><span data-stu-id="f256f-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="f256f-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="f256f-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-166">O método demonstra ao servidor EAP que uma única entidade agiu como o par EAP para todos os métodos executados em um método de túnel.</span><span class="sxs-lookup"><span data-stu-id="f256f-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="f256f-167">A associação também pode indicar que o servidor EAP demonstra ao par que uma única entidade agiu como o servidor EAP para todos os métodos executados em um método de túnel.</span><span class="sxs-lookup"><span data-stu-id="f256f-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="f256f-168">Se executado corretamente, a ligação serve para atenuar as vulnerabilidades do Man-in-the-Middle.</span><span class="sxs-lookup"><span data-stu-id="f256f-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span><span class="sxs-lookup"><span data-stu-id="f256f-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="f256f-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-171">O método demonstra que os ataques passivos (como captura da conversação EAP) ou ataques ativos (incluindo o comprometimento do MSK ou EMSK) não comprometem subseqüentes ou anteriores MSKs ou EMSKs.</span><span class="sxs-lookup"><span data-stu-id="f256f-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span><span class="sxs-lookup"><span data-stu-id="f256f-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="f256f-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-174">O método pode dar suporte à fragmentação e remontagem se os pacotes EAP excederem a MTU mínima (unidade de transmissão máxima) de 1020 octetos.</span><span class="sxs-lookup"><span data-stu-id="f256f-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="f256f-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f256f-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-177">O método pode comunicar Propriedades de canal protegidas por integridade, como identificadores de ponto de extremidade, que podem ser comparados a valores transmitidos usando mecanismos fora de banda, como uma [autenticação, autorização e contabilidade](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) ou o protocolo de camada inferior.</span><span class="sxs-lookup"><span data-stu-id="f256f-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span><span class="sxs-lookup"><span data-stu-id="f256f-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f256f-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="f256f-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-180">O método dá suporte à NAP (proteção de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="f256f-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span><span class="sxs-lookup"><span data-stu-id="f256f-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="f256f-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-183">O método pode ser usado em um computador autônomo.</span><span class="sxs-lookup"><span data-stu-id="f256f-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span><span class="sxs-lookup"><span data-stu-id="f256f-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="f256f-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="f256f-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-186">O método dá suporte à criptografia [de protocolo MPPE (criptografia ponto a ponto) da Microsoft](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="f256f-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span><span class="sxs-lookup"><span data-stu-id="f256f-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="f256f-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-189">O método dá suporte ao túnel de outros métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="f256f-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span><span class="sxs-lookup"><span data-stu-id="f256f-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="f256f-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-192">O método dá suporte a propriedades configuráveis e tem uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f256f-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span><span class="sxs-lookup"><span data-stu-id="f256f-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="f256f-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-195">O método foi certificado pelo programa de certificação EAP.</span><span class="sxs-lookup"><span data-stu-id="f256f-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="f256f-196">Esse bit só deve ser enviado por métodos EAP que passaram na certificação.</span><span class="sxs-lookup"><span data-stu-id="f256f-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span><span class="sxs-lookup"><span data-stu-id="f256f-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="f256f-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-199">Windows 7 ou posterior: o método pode ser usado para autenticar um computador em uma rede usando as credenciais de computadores.</span><span class="sxs-lookup"><span data-stu-id="f256f-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span><span class="sxs-lookup"><span data-stu-id="f256f-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="f256f-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-202">Windows 7 ou posterior: o método pode ser usado para autenticar um usuário em uma rede usando as credenciais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="f256f-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="f256f-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="f256f-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-205">Windows 7 ou posterior: o método dá suporte ao envio da identidade do usuário em um canal protegido.</span><span class="sxs-lookup"><span data-stu-id="f256f-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span><span class="sxs-lookup"><span data-stu-id="f256f-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="f256f-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-208">Windows 7 ou posterior: o método é um método tunnelled e dá suporte ao encadeamento de métodos EAP no túnel.</span><span class="sxs-lookup"><span data-stu-id="f256f-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span><span class="sxs-lookup"><span data-stu-id="f256f-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="f256f-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-211">Windows 7 ou posterior: o método dá suporte à equivalência de estado compartilhado, conforme definido no [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span><span class="sxs-lookup"><span data-stu-id="f256f-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f256f-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span><span class="sxs-lookup"><span data-stu-id="f256f-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f256f-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="f256f-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="f256f-214">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f256f-214">Reserved.</span></span> <span data-ttu-id="f256f-215">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f256f-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f256f-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f256f-216">Requirements</span></span>



| <span data-ttu-id="f256f-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="f256f-217">Requirement</span></span> | <span data-ttu-id="f256f-218">Valor</span><span class="sxs-lookup"><span data-stu-id="f256f-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f256f-219">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f256f-219">Minimum supported client</span></span><br/> | <span data-ttu-id="f256f-220">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f256f-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f256f-221">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f256f-221">Minimum supported server</span></span><br/> | <span data-ttu-id="f256f-222">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f256f-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f256f-223">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f256f-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="f256f-224"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f256f-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f256f-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="f256f-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f256f-226">Chaves do registro para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="f256f-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="f256f-227">Constantes do EAPHost comuns</span><span class="sxs-lookup"><span data-stu-id="f256f-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

