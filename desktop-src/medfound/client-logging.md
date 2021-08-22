---
description: Saiba mais sobre o log do cliente para Microsoft Media Foundation. O registro em log fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Log de cliente (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6e26d2034f87a6bf18fc626cdcdffec87da83cd20fe8a1a65db8d29f75f100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974995"
---
# <a name="client-logging-microsoft-media-foundation"></a>Log de cliente (Microsoft Media Foundation)

A fonte de rede dá suporte ao log do cliente, que fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele. Os logs do cliente permitem que um servidor Registre as estatísticas de conexão, renderização e streaming. Esses logs podem ser usados por provedores de conteúdo em vários cenários, como, para rastrear o uso do servidor de mídia e gerar cobrança, ou para fornecer conteúdo de qualidade adequado, dependendo da velocidade da rede do cliente.

Um arquivo de log contém várias entradas de evento de cliente. Cada entrada de log contém um número de campos delimitados por espaço. Há dois tipos de logs de cliente: *renderização* (em execução) e *streaming* (recebimento). Como o conteúdo pode ser reproduzido e transmitido simultaneamente, o cliente pode enviar uma combinação de ambos os tipos de dados de log. Em determinados casos, duas entradas de log podem existir para a mesma sessão. Por exemplo, quando o cache rápido está habilitado, o cliente pode concluir o recebimento do conteúdo transmitido antes de terminar de renderizá-lo. Nesse caso, os dados de log de streaming seriam enviados antes dos dados de log de renderização.

O cliente envia dados de log de renderização para o servidor quando o cliente muda de qualquer estado de reprodução (reprodução, avanço rápido ou retrocesso) para um estado de não execução (parar, pausar, fim do fluxo e início do fluxo). Quando os dados de um log de renderização são enviados, uma conexão é feita diretamente ao servidor de mídia ou a um servidor proxy configurado.

Se o conteúdo for armazenado em um arquivo de cache local temporário no computador que está executando o cliente, o cliente poderá ler um arquivo de seu cache local e enviar os dados de log de renderização para indicar que Ele reproduziu o conteúdo. Nesse caso, o cliente lê um arquivo de seu cache local, a entrada do log de renderização não contém nenhuma estatística de rede e o protocolo é definido como cache.

O cliente envia dados de log de streaming para o servidor para indicar como o cliente recebeu o conteúdo, mas não como ele foi renderizado. O cliente pode enviar o log de streaming longo antes que o cliente termine de renderizar o conteúdo.

Este tópico não fornece informações sobre todos os campos de log. para obter uma referência completa, consulte [Windows estrutura de dados de Log de mídia](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Configurando campos de log

Media Foundation permite que o cliente configure a origem da rede usando propriedades. O aplicativo deve definir as propriedades apropriadas em um repositório de propriedades e passá-lo para um dos métodos do resolvedor de origem. O resolvedor de origem cria a origem da rede conforme solicitado e abre uma conexão com o servidor. Se a conexão for bem-sucedida, o cliente enviará informações sobre si mesmo.

A tabela a seguir descreve os campos de log e as propriedades correspondentes que um aplicativo pode definir por meio do resolvedor de origem. Essas informações não são alteradas durante a sessão.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo de log</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Identificação exclusiva do Player. Essas informações são enviadas no início da conexão. Normalmente, esse é um GUID do cliente. O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .<br/> O cliente envia essas informações ao servidor no início da conexão.<br/> Valor de exemplo: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>O número de versão do Player que é enviado no início da conexão. O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .<br/> O cliente envia essas informações ao servidor no início da conexão.<br/></td>
</tr>
<tr class="odd">
<td>CS (agente do usuário)</td>
<td>Tipo de navegador usado se o Player foi inserido em um navegador. Esse valor pode ser definido pelo cliente na propriedade <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .<br/> Se o Player não tiver sido inserido, esse campo se referirá ao agente de usuário do cliente que gerou o log. Nesse caso, o cliente deve definir a propriedade <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .<br/> O cliente envia essas informações ao servidor no início da conexão.<br/> Valor de exemplo: &quot; Mozilla/4.0 _ (compatível; _MSIE_4.01; _Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>CS (referenciador)</td>
<td>URL da página da Web na qual o Player foi inserido (se foi inserido). O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .<br/> O cliente envia essas informações ao servidor no final da conexão.<br/> Valor de exemplo: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Para entradas de log do Player, o programa de host (.exe) que foi executado. por exemplo, uma página da web em um navegador, um miniaplicativo do Microsoft Visual Basic ou um player autônomo. O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .<br/> O cliente envia essas informações ao servidor no final da conexão.<br/> Valores de amostra:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Número de versão do .exe (programa de host). O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .<br/> O cliente envia essas informações ao servidor no final da conexão.<br/></td>
</tr>
</tbody>
</table>



 

O exemplo de código a seguir mostra como um aplicativo cliente configura a origem da rede. Este exemplo define o campo de log "c-hostexe".


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>Recuperando estatísticas de rede

Quando o aplicativo chama um dos métodos do resolvedor de origem, ele cria a origem da rede, define as propriedades especificadas no repositório de propriedades e abre uma sessão com o servidor de mídia. Além das informações configuráveis descritas na seção anterior, os dados adicionais são transferidos entre o servidor e o cliente no início da sessão, durante o streaming e quando a sessão é fechada.

O aplicativo pode recuperar estatísticas de rede usando o identificador de serviço do **\_ \_ serviço de estatísticas MFNETSOURCE** . Para usar esse serviço, o aplicativo pode chamar a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o repositório de propriedades que contém as estatísticas de rede na propriedade de [**\_ estatísticas MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . Valores específicos podem ser recuperados fornecendo o identificador correspondente definido na enumeração **de \_ \_ IDs de estatísticas MFNETSOURCE** .

O exemplo de código a seguir mostra como usar o serviço para obter o número de pacotes recebidos pelo cliente.


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



A lista a seguir descreve alguns dos identificadores de estatísticas de rede definidos nas [**\_ \_ IDs de estatísticas do MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificador de estatísticas de rede              | Descrição                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**       | Largura de banda média (em bits por segundo) na qual o cliente foi conectado ao servidor. O valor é calculado em toda a duração da conexão.                                                              |
| **MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**        | Número de vezes que o cliente bufferu ao reproduzir o fluxo.                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ ID**         | Número de bytes recebidos pelo cliente do servidor. O valor não inclui nenhuma sobrecarga que é adicionada pela pilha de rede. O mesmo conteúdo transmitido usando protocolos diferentes pode resultar em valores diferentes. |
| **MFNETSOURCE \_ LINKBANDWIDTH \_ ID**         | Largura de banda máxima disponível do cliente em bits por segundo.                                                                                                                                                              |
| **MFNETSOURCE \_ LOSTPACKETS \_ ID**           | Número de pacotes enviados pelo servidor, mas perdidos durante a transmissão, e nunca reproduzidos pelo cliente. O valor não inclui pacotes TCP ou UDP.                                                                          |
| **MFNETSOURCE \_ RECVPACKETS \_ ID**           | Número de pacotes recebidos do servidor o valor não inclui pacotes TCP ou UDP.                                                                                                                                  |
| **MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ ID** | Pacotes perdidos na rede que foram reparados e recuperados na camada do cliente. Esse valor não inclui pacotes TCP ou UDP.                                                                                          |
| **MFNETSOURCE \_ RESENDSREQUESTED \_ ID**      | O número de solicitações feitas pelo cliente para receber novos pacotes. Esse valor não inclui pacotes TCP ou UDP.                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**      | Número de pacotes recuperados porque eles foram reenviados por meio de UDP. Esse valor não inclui pacotes TCP ou UDP. Este campo contém um zero, a menos que o cliente esteja usando o reenvio de UDP.                                        |
| **MFNETSOURCE \_ BUFFERPROGRESS \_ ID**        | A porcentagem do buffer de reprodução preenchida durante o armazenamento em buffer.                                                                                                                                                              |
| **\_ID do protocolo MFNETSOURCE \_**              | Protocolo usado para acessar o fluxo. Isso pode ser diferente do protocolo solicitado pelo cliente.                                                                                                                             |
| **\_ID de transporte MFNETSOURCE \_**             | Protocolo de transporte usado para entregar o fluxo. Deve ser UDP ou TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de origem da rede](network-source-features.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

