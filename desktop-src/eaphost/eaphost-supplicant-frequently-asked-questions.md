---
title: Perguntas frequentes sobre suplicantes do EAPHost
description: Este tópico fornece respostas para as perguntas mais frequentes sobre a API suplicante do EAPHost.
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103643099"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a>Perguntas frequentes sobre suplicantes do EAPHost

Este tópico fornece respostas para as perguntas mais frequentes sobre a API suplicante do EAPHost.

### <a name="eaphost-supplicant-frequently-asked-questions"></a>Perguntas frequentes sobre suplicantes do EAPHost



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
<td>Por que preciso chamar [<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) e [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize)?</td>
<td>[<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) e [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) inicializam e não inicializam o ambiente com usado para comunicação entre processos (IPC) entre um suplicante e o EAPHost.</td>
</tr>
<tr class="even">
<td>Quais funções devem ser invocadas em threads que têm inicializado COM para [single-threaded apartment](/previous-versions/ms810413(v=msdn.10)) (STA)?</td>
<td>[<strong>EapHostPeerInvokeConfigUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) e [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodauthenticatorapis/NF-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) devem ser chamados em threads com inicializado com para STA. Isso pode ser obtido chamando a API COM [<strong>CoInitialize</strong>] (/Windows/Win32/API/Objbase/NF-Objbase-CoInitialize); Quando o suplicante for concluído com o thread STA [<strong>CoUninitialize</strong>] (/Windows/Win32/API/combaseapi/NF-combaseapi-CoUninitialize) deve ser chamado antes de sair.</td>
</tr>
<tr class="odd">
<td>Como o EAPHost exporta o material de chave?</td>
<td>Os métodos de EAP do EAPHost exportam chaves de sessão mestre (MSKs) na forma de chaves MPPE (criptografia ponto a ponto) da Microsoft para os suplicantes. Material de chave adicional, como PMKs (chaves mestras de paridade), podem ser gerados pelo suplicante usando o MSK. Para que os métodos gerem outras chaves durante a autenticação, os métodos podem fornecer essas chaves como atributos específicos do fornecedor aos suplicantes.</td>
</tr>
<tr class="even">
<td>O que é uma chave de sessão mestre estendida (EMSK)?</td>
<td>EMSK é material de chave adicional que é exportado pelo método EAP. EMSK tem pelo menos 64 octetos de comprimento. O EMSK é compartilhado entre o cliente e o servidor EAP, mas não é compartilhado com o autenticador ou com terceiros. Atualmente, o EMSK está reservado para uso futuro. Para obter mais informações, consulte [requisitos do método EAP (Extensible Authentication Protocol) para LANs sem fio](https://go.microsoft.com/fwlink/p/?linkid=84064).<br/></td>
</tr>
<tr class="odd">
<td>Quando um método consome ou gera um atributo?</td>
<td>Se um método EAP gerar atributos ou EMSK, o suplicante consumirá atributos. Normalmente, os atributos consumidos por suplicantes são chaves. Os atributos consumidos são <strong>eatPeerId</strong>, <strong>eatServerId</strong>, <strong>eatMethodId</strong>, <strong>eatEMSK</strong>e <strong>eatCredentialsChanged</strong>. Para obter mais informações, consulte [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type). Um método EAP pode exportar material de EMSK específico do aplicativo adicional, como:
<ul>
<li>ID da sessão</li>
<li>NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) )</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Quais atributos o [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) consome?</td>
<td>O suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) nativo sem fio consumirá os seguintes atributos de autenticação do EAPHost:
<ul>
<li>Notificação de alteração de senha</li>
<li>Chaves de envio/recebimento de MPPE (criptografia ponto a ponto) da Microsoft. VendorID/Vendor = 331/16 e 311/1</li>
</ul>
As chaves MPPE são chaves geradas no final da autenticação bem-sucedida, tanto no peer quanto no autenticador. Essas chaves são usadas pelo [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e pelo nas (servidor de acesso à rede) para criptografar e descriptografar pacotes que são enviados e recebidos.<br/></td>
</tr>
<tr class="odd">
<td>Qual é a finalidade do sinalizador de EAP_PEER_FLAG_GUEST_ACCESS no EAPHost?</td>
<td>Quando esse sinalizador é definido em [<strong>EAPHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession), o EAPHost interpreta isso como uma solicitação de autorização de convidado e retorna uma resposta de identidade <strong>nula</strong> que é passada para o suplicante e retornada ao servidor EAP.</td>
</tr>
<tr class="even">
<td>Como o suplicante solicita autenticação do computador?</td>
<td>A autenticação do computador é solicitada definindo o sinalizador [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="odd">
<td>Como o suplicante solicita autenticação de usuário?</td>
<td>A autenticação do usuário é solicitada por não definir o sinalizador [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="even">
<td>Quando usar [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) em vez da função [<strong>EapHostFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror)?</td>
<td>A função [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) é usada somente para estruturas [<strong>EAP_ERROR</strong>] (/Windows/Desktop/API/eaptypes/NS-eaptypes-eap_error) de liberação retornadas pelas APIs de configuração do EAPHost. As APIs de configuração do EAPHost são definidas em EapHostPeerConfigApis. h. Por outro lado, a função [<strong>EapHostPeerFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror) é usada para liberar <strong>EAP_ERROR</strong> estruturas retornadas por APIs de tempo de execução do EAPHost. As APIs de tempo de execução do EAPHost são definidas em EapPApis. h. Nunca use a versão de tempo de execução da API com a versão de configuração das APIs; Isso pode gerar resultados inesperados.<br/></td>
</tr>
<tr class="odd">
<td>Implementei minha interface do usuário no mesmo thread que uso para processar uma sessão de autenticação EAP no suplicante. Depois de ter gerado uma caixa de diálogo de interface do usuário interativa para obter credenciais ou outros dados de entrada do usuário, a próxima chamada do EAPHost para um método EAP peer falhará com <strong>ERROR_OBJECT_DISCONNECTED</strong>. Por que isso ocorreu e como solucioná-lo?</td>
<td>Embora as APIs do lado do cliente do EAPHost sejam todas APIs de estilo C, essas APIs C são apenas wrappers de APIs COM correspondentes. As APIs de estilo C são executadas em um ambiente COM multithread. O código da interface do usuário geralmente é executado no modelo de thread apartment. Como os dois modelos de thread entram em conflito uns com os outros, não execute o código da interface do usuário no mesmo thread que processa as autenticações EAP.</td>
</tr>
<tr class="even">
<td>Por que a API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) pega um ponteiro de função de retorno de chamada [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) como um parâmetro?</td>
<td>[<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) é o mecanismo pelo qual um suplicante é notificado de que ele deve autenticar novamente. Há vários cenários em que o suplicante é necessário para autenticar novamente, incluindo a autenticação com NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ).</td>
</tr>
<tr class="odd">
<td>Qual é a finalidade do parâmetro <em>pConnectionId</em> na API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession)?</td>
<td><em>pConnectionId</em> é um ponteiro para um valor GUID definido pelo suplicante usado para identificar uma conexão de rede que pertence ao suplicante. Quando a função de retorno de chamada [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) é chamada, esse GUID é passado para identificar a conexão de rede que o suplicante usará para solicitações de nova autenticação.</td>
</tr>
<tr class="even">
<td>Como fazer saber se há uma alteração no estado de quarentena?</td>
<td>O usuário receberá uma notificação visual de uma alteração no estado de quarentena somente se houver pelo menos uma interface registrada do cliente de imposição de quarentena (NAP) QEC (proteção de acesso à rede) no sistema. Nesse caso, quando a nova autenticação for tentada, o usuário será notificado sobre uma alteração de estado de quarentena por meio de uma janela pop-up.</td>
</tr>
<tr class="odd">
<td>Como fazer saber se há uma interface QEC registrada em NAP no sistema?</td>
<td>Abra uma janela com privilégios elevados e execute o seguinte comando netsh: &quot; netsh nap client mostrar estado &quot; . Para obter mais informações, consulte [comandos netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Se o suplicante autenticar novamente, qual ID de conexão deve ser usada pelo QEC durante a nova autenticação?</td>
<td>O QEC deve usar a mesma ID de conexão usada para a sessão anterior.</td>
</tr>
<tr class="odd">
<td>Há apenas um método do suplicante do EAPHost disponível para exibir caixas de diálogo da interface do usuário, mas os métodos EAP têm vários tipos de chamadas específicas à interface de usuários. Qual método deve ser chamado pelo suplicante ao obter o código de ação <strong>EapHostPeerResponseInvokeUI</strong> , indicando que o suplicante deve exibir uma caixa de diálogo de interface do usuário?</td>
<td>Nenhuma ação é exigida pelo usuário porque o EAPHost sabe qual função de método deve ser chamada. Por exemplo, quando o código de ação <strong>EapHostPeerResponseInvokeUI</strong> é retornado, o suplicante chama essas três funções na seguinte ordem: [<strong>EapHostPeerGetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeergetuicontext), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) e [<strong>EapHostPeerSetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeersetuicontext).</td>
</tr>
<tr class="even">
<td>Qual é a diferença entre um BLOB de credenciais e um BLOB de configuração?</td>
<td>O BLOB de credenciais contém apenas dados de usuário, como nome de usuário, senha e PIN. O BLOB de configuração contém as configurações que controlam o comportamento do método.</td>
</tr>
<tr class="odd">
<td>Posso habilitar o rastreamento no lado do cliente EAPHost?</td>
<td>Sim. Para obter mais informações, consulte [habilitando o rastreamento](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API do suplicante EAPHost](eap-host-supplicant-api-reference.md)
</dt> <dt>

[Perguntas frequentes sobre o EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[FAQs do método EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Perguntas frequentes de desenvolvimento do EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

