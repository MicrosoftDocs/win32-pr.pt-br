---
title: Perguntas frequentes gerais
description: Leia as respostas para as perguntas mais frequentes sobre as APIs do EAPHost, como ' Qual é o tempo de vida de uma autenticação? '.
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105812034"
---
# <a name="general-frequently-asked-questions"></a>Perguntas frequentes gerais

O tópico a seguir fornece respostas para perguntas mais frequentes sobre as APIs do EAPHost.

### <a name="general-frequently-asked-questions"></a>Perguntas frequentes gerais



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pergunta</th>
<th>Resposta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>O que é um suplicante?</td>
<td>O suplicante é a entidade a ser autenticada usando o EAPHost. Os suplicantes típicos são clientes [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , 802,3 clientes e RRAS (serviço de roteamento e acesso remoto), clientes de ponto a ponto (PPP).</td>
</tr>
<tr class="even">
<td>O que é um par?</td>
<td>O par é o lado do cliente de uma autenticação EAP.</td>
</tr>
<tr class="odd">
<td>Como um par difere de um suplicante?</td>
<td>O suplicante transporta pacotes, enquanto um par não. No entanto, os termos par, suplicante e cliente são amplamente sinônimos.</td>
</tr>
<tr class="even">
<td>O que é um autenticador?</td>
<td>O autenticador é o ponto de acesso sem fio, o NAS (servidor de acesso à rede) ou o NAD (dispositivo de acesso à rede) que autentica o suplicante. O autenticador também é conhecido como o servidor EAP.</td>
</tr>
<tr class="odd">
<td>Qual é o tempo de vida de uma autenticação?</td>
<td>O tempo de vida de uma única sessão de autenticação no lado do cliente é tudo o que ocorre entre as funções [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) e [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) que estão sendo chamadas. O tempo de vida no lado do autenticador é tudo o que ocorre entre as funções [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) e [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</td>
</tr>
<tr class="even">
<td>O que é um BLOB? Por que eu converteria um BLOB de configuração (binário) em XML?</td>
<td>Um BLOB é um objeto binário grande. O XML tem várias vantagens em relação a um BLOB de configuração binária. Os dados de configuração armazenados em XML são legíveis, humanos-editable e de plataforma cruzada.</td>
</tr>
<tr class="odd">
<td>Quando converto um BLOB XML armazenado de volta em um BLOB binário?</td>
<td>É possível armazenar um blob binário ou BLOB XML, mas você sempre deve converter o BLOB XML de volta em um BLOB binário antes de usá-lo com APIs de tempo de execução; as APIs de tempo de execução não podem aceitar um diretório XML.</td>
</tr>
<tr class="even">
<td>O que são métodos nativos?</td>
<td>Os métodos EAP nativos usam a nova API EAPHost.</td>
</tr>
<tr class="odd">
<td>O que são métodos herdados?</td>
<td>Os métodos EAP herdados são definidos na [referência do protocolo de autenticação extensível](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference). Os métodos EAP herdados estão disponíveis para uso no Windows Vista e no Windows Server 2008. Esses métodos podem não estar disponíveis para uso em versões subsequentes do sistema operacional.</td>
</tr>
<tr class="even">
<td>Qual é a diferença entre os métodos herdados e nativos?</td>
<td>As APIs nativas são mais simples e têm menos recursos. Todos os novos métodos EAP devem ser escritos usando a API EAPHost.</td>
</tr>
<tr class="odd">
<td>O que é &quot; diretiva de grupo &quot; ?</td>
<td>Para obter uma descrição da diretiva de grupo, consulte [política de grupo coleção](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</td>
</tr>
<tr class="even">
<td>As funções EAPHost podem substituir a política de configuração especificada pela política de grupo?</td>
<td>Não, nunca. Se a política de grupo estiver em uso, as configurações da política de grupo sempre substituirão as definições de configuração do EAPHost.</td>
</tr>
<tr class="odd">
<td>O que é SSO (logon único)?</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) é um mecanismo de autenticação de camada 2. Dependendo da configuração de SSO, o SSO permite que os usuários se autentiquem na rede usando a autenticação [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) antes ou imediatamente após o logon no Windows. O SSO pode ser configurado para usar credenciais do Windows para autenticação de rede (nesse caso, os usuários inserem suas credenciais apenas uma vez) ou usam credenciais diferentes para o Windows e a autenticação de rede. Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).<br/></td>
</tr>
<tr class="even">
<td>O que é provedor de acesso pré-logon (PLAP)</td>
<td>Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).</td>
</tr>
<tr class="odd">
<td>O que é PEAP (protocolo de autenticação extensível protegida)?</td>
<td>Para obter mais informações, consulte [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) e [sobre o protocolo de autenticação extensível](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</td>
</tr>
<tr class="even">
<td>Como o PEAP lida com a retomada da sessão e a nova autenticação?</td>
<td>A retomada da sessão e a nova autenticação normalmente ocorrem durante o roaming em uma rede sem fio. A API de proteção de dados do Windows (DPAPI) fornece uma maneira de proteger e associar dados a um usuário e, opcionalmente, à sessão de logon. O chamador dá ao [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) um buffer não criptografado, e a DPAPI criptografará a memória no local. Posteriormente, o chamador pode passar o buffer criptografado para [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) e a DPAPI descriptografará a memória, novamente no lugar. Para obter mais informações, consulte [extensão de aplicativo interno TLS (TSL/ia)](https://go.microsoft.com/fwlink/p/?linkid=84011) e [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).<br/></td>
</tr>
<tr class="odd">
<td>O que é o EAP-TLS (segurança de nível EAP-Transport)?</td>
<td>O EAP-TLS é um protocolo de cliente-servidor no qual os perfis de certificado distintos normalmente são usados para o cliente e o servidor. Para obter mais informações, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/></td>
</tr>
<tr class="even">
<td>Como fazer implementar uma alteração de senha usando a API da autoridade de segurança local (LSA)?</td>
<td>Use a função [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) para implementar uma alteração de senha.</td>
</tr>
<tr class="odd">
<td>Por que desejo habilitar o rastreamento no EAPHost?</td>
<td>Os logs de rastreamento contêm informações de depuração (disponíveis somente em inglês) que podem ajudar os desenvolvedores e parceiros da Microsoft a encontrar as causas raiz de quaisquer problemas com o processo de autenticação. Para obter mais informações, consulte [habilitando o rastreamento](enabling-tracing.md).<br/></td>
</tr>
<tr class="even">
<td>Por que encontro o código de erro, NTE_BAD_KEY_STATE (0x8009000BL) quando uso a API de [criptografia](/windows/desktop/SecCrypto/cryptography-portal) para entrar no Exchange EAP-TLS?</td>
<td>No Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) é definido como uma &quot; chave não válida para uso no estado especificado &quot; . Esse erro normalmente é retornado nos cenários a seguir.
<ul>
<li>Ao tentar exportar um BLOB de chave privada não exportável</li>
<li>Quando a tentativa de gerar um identificador de hash de uma função pseudo aleatória (PRF) não é bem-sucedida usando [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/WinCrypt/NF-WinCrypt-CryptCreateHash)</li>
</ul>
Para obter mais informações, consulte [concluir mensagens no protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</td>
</tr>
<tr class="odd">
<td>O que é uma função pseudo aleatória (PRF)?</td>
<td>Uma função que usa uma chave, rótulo e semente como entrada e produz uma saída de comprimento arbitrário. Para obter mais informações, consulte [concluir mensagens no protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).<br/></td>
</tr>
<tr class="even">
<td>Como o EAPHost se associa a adaptadores de rede?</td>
<td>O EAPHost permite que vários suplicantes operem simultaneamente, e cada suplicante pode se associar a vários adaptadores de rede. Os suplicantes do EAPHost fornecem associação às camadas de rede e orientam o processo de autenticação. Os suplicantes contêm configuração de autenticação. Os suplicantes também salvam o estado e fornecem segurança de conexão subsequente. Como o EAPHost não se associa diretamente a nenhum mecanismo de rede, a extensibilidade do suplicante é possível.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes do suplicante do EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[FAQs do método EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Perguntas frequentes de desenvolvimento do EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

