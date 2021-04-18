---
title: Perguntas frequentes sobre o método EAP
description: Fornece respostas para perguntas de programação mais frequentes sobre a criação de métodos EAP.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105796079"
---
# <a name="eap-method-frequently-asked-questions"></a>Perguntas frequentes sobre o método EAP

Este tópico fornece respostas para perguntas de programação mais frequentes sobre a criação de métodos EAP.

## <a name="eap-method-frequently-asked-questions"></a>Perguntas frequentes sobre o método EAP



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
<td>O que são &quot; os dados de configuração &quot; ?</td>
<td>Os termos &quot; dados de configuração &quot; e &quot; dados de conexão &quot; são sinônimos.</td>
</tr>
<tr class="even">
<td>O que são &quot; os dados de conexão &quot; ?</td>
<td>&quot;Os dados de conexão &quot; são um blob opaco específico de método EAP que contém informações de configuração para o método. Esses dados de conexão são criados pelo método quando ele é inicialmente configurado e nunca são interpretados ou modificados por qualquer outro componente do que o próprio método EAP.</td>
</tr>
<tr class="odd">
<td>O que são &quot; credenciais &quot; ?</td>
<td>Os termos &quot; credenciais &quot; e &quot; dados de usuário &quot; são sinônimos.</td>
</tr>
<tr class="even">
<td>O que são &quot; os dados do usuário &quot; ?</td>
<td>&quot;Os dados do usuário &quot; são um blob opaco específico do método EAP que contém dados de credenciais do usuário, como um nome de usuário e senha. Os dados do usuário nunca são interpretados ou modificados por qualquer outro componente do que o próprio método EAP. Os termos &quot; dados &quot; e credenciais do usuário &quot; &quot; são sinônimos.</td>
</tr>
<tr class="odd">
<td>O que é um &quot; atributo EAP &quot; ?</td>
<td>Um &quot; atributo EAP &quot; é uma estrutura de dados que contém um tipo de dados predeterminado. Os atributos são usados para comunicar informações entre os métodos EAP e suplicantes, ou entre os métodos EAP e autenticadores. As implementações de ponto e autenticador de um método EAP podem trocar esses atributos por uma rede.</td>
</tr>
<tr class="even">
<td>A API de configuração e a API de tempo de execução aparecem no mesmo método DLL?</td>
<td>Sim. Certifique-se de especificar a distinção ao configurar as entradas do registro para o próprio método EAP. O caminho de configuração e o caminho de par devem ser iguais.</td>
</tr>
<tr class="odd">
<td>A API de configuração e a API de tempo de execução aparecem em DLLs de método separadas?</td>
<td>Sim. Certifique-se de especificar a distinção ao configurar as entradas do registro para o próprio método EAP. Os caminhos de configuração e ponto a ponto devem apontar para as DLLs corretas.</td>
</tr>
<tr class="even">
<td>Como fazer instalar um método EAP?</td>
<td>Para instalar um método EAP, você deve primeiro implementar [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllRegisterServer) e [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DLLUNREGISTERSERVER) na própria DLL do método EAP. Depois disso, use <strong>regsvr32.exe</strong> para instalar e desinstalar o método. As chaves de registro apropriadas também devem ser definidas. Para obter mais informações, consulte [instalando um método EAP](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>O que é o suporte a NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) )?</td>
<td>Quando o suporte a NAP em banda está habilitado, os pacotes NAP são transportados dentro de pacotes de método EAP. Por outro lado, quando o suporte a NAP fora de banda está habilitado, a troca de soh ( [instrução NAP de integridade](https://go.microsoft.com/fwlink/p/?linkid=83917) ) ocorre por meio de meios diferentes de pacotes de método EAP e certificados gerados por NAP são usados na autenticação do método EAP.</td>
</tr>
<tr class="even">
<td>Posso habilitar o suporte a NAP em banda para o meu método EAP?</td>
<td>Sim, o suporte a NAP em banda para o método EAP pode ser habilitado. Para obter mais informações, consulte [habilitando o suporte a In-Band NAP para métodos EAP](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>Como funciona a autenticação flexível do EAP por meio de túnel seguro (EAP-FAST)?</td>
<td>O cenário EAP-FAST funciona da seguinte maneira. <br/>
<ul>
<li>O método processa uma alteração de senha em SSO (logon único) empregando a interface do usuário do método.</li>
<li>O método retorna o atributo [<strong>eatCredentialsChanged</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type).</li>
<li>O suplicante indica ao usuário que as credenciais foram alteradas e solicita que o usuário insira novamente suas credenciais.</li>
<li>O suplicante insere novamente as credenciais do usuário e envia essas credenciais para o método.</li>
</ul>
Para obter mais informações sobre EAP-FAST, consulte [autenticação flexível do EAP por meio de túnel seguro](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-FAST).</td>
</tr>
<tr class="even">
<td>O que é a PSK (chave pré-compartilhada)?</td>
<td>Um método de transmissão e recebimento de sinais digitais em que a fase de um sinal transmitido é variada para transmitir informações. O campo de entrada [<strong>EAPConfigInputPSK</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_config_input_field_type) contém o PSK EAP-FAST do usuário.</td>
</tr>
<tr class="odd">
<td>O que é WOW e como isso é importante para o EAPHost?</td>
<td>O Microsoft Windows-32-bit-on-Windows-64-bit (WOW) é um componente do sistema operacional no Windows de 64 bits que dá suporte ao aplicativo de plataforma x86 de 32 bits. Normalmente, um autor de método EAP definiria alguma forma de estrutura C/C++ para encapsular dados de configuração, dados de credenciais e dados interativos da interface do usuário. Para evitar incompatibilidades no WOW e em outros cenários, é importante garantir que as estruturas de dados estejam alinhadas da mesma forma em diferentes arquiteturas de processador (processadores de 32 bits e 64 bits). Normalmente, o preenchimento fictício é usado para alinhar os campos de forma que a configuração, a credencial e os dados da interface do usuário interativa sejam idênticos nos processadores de 32 e 64 bits.</td>
</tr>
<tr class="even">
<td>O que são os &quot; códigos &quot; de ação e em quais condições esses códigos de ação são retornados?</td>
<td>&quot;Os códigos &quot; de ação permitem que os métodos controlem o fluxo de autenticação e são integrantes à máquina de estado. Eles são valores retornados por um método EAP para indicar a próxima ação que o EAPHost deve executar. Por exemplo, um código de ação poderia indicar o EAPHost de que o método EAP tem um pacote pronto para transmissão. O suplicante obedece a todos os códigos de ação retornados por um método EAP, mas nunca emite os códigos de ação. Para obter mais informações, consulte [códigos de ação suplicante de peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que ele deve descartar o pacote fornecido para o método. Especificamente, o método determinou que o pacote é inválido. O EAPHost aguarda o próximo pacote.</td>
</tr>
<tr class="even">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que o próximo pacote recebido pelo EAPHost deve ser enviado ao NAS (servidor de acesso à rede).</td>
</tr>
<tr class="odd">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que a sessão de autenticação concluiu e que os resultados dessa sessão estão disponíveis.</td>
</tr>
<tr class="even">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que a entrada do usuário é necessária para continuar com a autenticação e que uma caixa de diálogo da interface do usuário deve ser exibida para obter essa entrada. Depois que os dados de entrada do usuário forem obtidos, o EAPHost poderá chamar o método EAP novamente com os dados de contexto da interface do usuário atualizados.</td>
</tr>
<tr class="odd">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que o método EAP tem atributos disponíveis para uso do EAPHost durante a autenticação. O EAPHost Obtém os atributos chamando o método [<strong>EapPeerGetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeergetresponseattributes) seguido por uma chamada para o método [<strong>EapPeerSetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes).</td>
</tr>
<tr class="even">
<td>Quando um método retorna [<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e o que esse código de ação significa para o EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) é retornado por um método EAP para indicar ao EAPHost que nenhuma ação é necessária no momento.</td>
</tr>
<tr class="odd">
<td>Posso habilitar o rastreamento no lado do autenticador?</td>
<td>Sim. Para obter mais informações, consulte [habilitando o rastreamento](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API do método par do EAPHost](eap-host-peer-method-api-reference.md)
</dt> <dt>

[Perguntas frequentes sobre o EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Perguntas frequentes do suplicante do EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Perguntas frequentes de desenvolvimento do EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

