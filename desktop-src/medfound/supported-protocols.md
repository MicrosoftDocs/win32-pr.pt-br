---
description: Protocolos compatíveis
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos compatíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b086b48b73c0412968c00091e6353d134006f45fa9c8b8f229ea3f9e695bf99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238123"
---
# <a name="supported-protocols"></a>Protocolos compatíveis

O Media Foundation dá suporte aos seguintes protocolos:

-   Protocolo RTSP (real time streaming)

    O RTSP é usado principalmente para transmitir conteúdo de mídia. Ele pode usar UDP ou TCP como protocolos de transporte. O UDP é o mais eficiente para a entrega de conteúdo porque a sobrecarga de largura de banda é menor do que com protocolos baseados em TCP. Embora o protocolo TCP garanta uma entrega de pacotes confiável, o TCP não é adequado para fluxos de mídia digital, onde o uso eficiente da largura de banda é mais importante do que os pacotes perdidos ocasionais.

-   Protocolo HTTP

    O HTTP usa TCP e é usado por servidores Web. O esquema "httpd://" indica que a origem pode ser baixada de um servidor Web. O HTTP também é usado no caso de firewalls, que geralmente são configurados para aceitar solicitações HTTP e normalmente rejeitam outros protocolos de streaming.

O aplicativo pode obter os protocolos com suporte pelo Media Foundation usando a interface [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) . Para fazer isso, o aplicativo deve primeiro recuperar o número de protocolos, chamando [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) e obter o tipo de protocolo com base no índice chamando [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Esse método retorna um dos valores definidos na enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .

O aplicativo também pode obter os esquemas suportados pelo resolvedor de origem chamando a função [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .

## <a name="protocol-rollover"></a>Substituição de protocolo

Quando um aplicativo especifica "mms://" como o esquema de URL, o resolvedor de origem executa uma operação de *substituição de protocolo* . Nesse processo, o resolvedor de origem determina o melhor protocolo para a fonte de rede usar para obter o conteúdo. Normalmente, para o fluxo de mídia, o RTSP com UDP (RTSPu) é mais eficiente do que o HTTP. No entanto, se o conteúdo estiver hospedado em um servidor Web, o HTTP será uma opção melhor.

A substituição de protocolo também pode ocorrer quando uma tentativa de usar o protocolo especificado no esquema de URL falha. Por exemplo, um protocolo pode falhar quando um firewall bloqueia pacotes UDP. Nesse caso, o resolvedor de origem alterna para HTTP.

A substituição de protocolo não se aplicará se o esquema de URL contiver um protocolo específico, como "rtspu://". Além disso, a substituição não será executada se a autenticação falhar ou se o servidor tiver atingido um limite de conexões de cliente. É recomendável que os aplicativos especifiquem o esquema "mms://" e permitam que o resolvedor de origem selecione o melhor protocolo para o cenário.

A tabela a seguir lista a ordem de sobreposição.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esquemas permitidos</th>
<th>Ordem de substituição de protocolo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms://ou rtsp://</td>
<td>Cache rápido habilitado:<br/>
<ol>
<li>RTSP com TCP (RTSPt)<br/></li>
<li>RTSP com UDP (RTSPu)<br/></li>
<li>Streaming HTTP<br/></li>
<li>Download de HTTP (HTTP)<br/></li>
</ol>
Cache rápido desabilitado:<br/>
<ol>
<li>RTSPu<br/></li>
<li>RTSPt<br/></li>
<li>Streaming HTTP<br/></li>
<li>Download de HTTP<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>RTSPu</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPt</td>
</tr>
<tr class="even">
<td>https://</td>
<td><ol>
<li>HTTP<br/></li>
<li>HTTPD<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>httpd://</td>
<td>HTTPD</td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a>Recuperando o protocolo atual

Após uma operação de substituição de protocolo, a origem da rede pode usar um protocolo diferente daquele especificado pelo aplicativo no esquema de URL. O resultado da substituição de protocolo está disponível para o aplicativo depois que a fonte de rede estabelece a conexão com o servidor de mídia.

Para obter o protocolo e o transporte que são usados para obter o conteúdo, o aplicativo pode recuperar os valores de propriedade para a propriedade de [ \_ protocolo MFNETSOURCE](mfnetsource-protocol-property.md) e a propriedade de [ \_ transporte MFNETSOURCE](mfnetsource-transport-property.md) de um objeto **IPropertyStore** da fonte de rede.

O código a seguir mostra como obter esses valores.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



No código de exemplo anterior, **IPropertyStore:: GetValue** recupera o \_ valor do protocolo MFNETSOURCE, que é um membro da enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) . Para o \_ transporte MFNETSOURCE, o valor é um membro da enumeração de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .

Como alternativa, o aplicativo pode obter os mesmos valores usando o serviço de \_ estatísticas MFNETSOURCE \_ . Para usar esse serviço, o aplicativo pode chamar a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o repositório de propriedades da fonte de rede. Esse repositório de propriedades contém estatísticas de rede na propriedade [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) . Os valores de protocolo e transporte podem ser recuperados \_ especificando \_ -se a ID do protocolo MFNETSOURCE e \_ a ID de transporte MFNETSOURCE \_ — definidas na enumeração [**\_ \_ IDs de estatísticas MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . O código a seguir mostra como obter os valores de protocolo e transporte usando o \_ serviço de serviço de estatísticas MFNETSOURCE \_ .


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Habilitando e desabilitando protocolos

O aplicativo pode configurar a origem da rede para que determinados protocolos sejam ignorados durante o processo de substituição. Para fazer isso, as propriedades de origem da rede são usadas para desabilitar protocolos específicos. A tabela a seguir mostra as propriedades e os protocolos que eles controlam.



| Propriedade                                                                    | Descrição                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ habilitar \_ http](mfnetsource-enable-http-property.md)           | Habilita ou desabilita HTTP e HTTP.         |
| [MFNETSOURCE \_ habilitar \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Habilita ou desabilita o RTSPu e o RTSPt.        |
| [MFNETSOURCE \_ habilitar \_ TCP](mfnetsource-enable-tcp-property.md)             | Habilita ou desabilita o RTSPt.                  |
| [MFNETSOURCE \_ habilitar \_ UDP](mfnetsource-enable-udp-property.md)             | Habilita ou desabilita o RTSPu.                  |
| [MFNETSOURCE \_ habilitar \_ Download](mfnetsource-enable-download-property.md)   | Habilita ou desabilita o HTTP.                  |
| [MFNETSOURCE \_ habilitar \_ streaming](mfnetsource-enable-streaming-property.md) | Habilita ou desabilita o RTSPu, o RTSPt e o HTTP. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




