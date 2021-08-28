---
title: Tipo complexo ChannelType
description: Define um canal para o qual os provedores podem registrar eventos.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- Tipo complexo ChannelType EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b780d68d419fa29d5ee13995f1b66a412fc89323
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627962"
---
# <a name="channeltype-complex-type"></a>Tipo complexo ChannelType

Define um canal para o qual os provedores podem registrar eventos.

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                  | Type                                                                                   | Descrição                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Log**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Define as propriedades do arquivo de log que faz o retorno do canal, como sua capacidade e se o arquivo de log é sequencial ou circular.<br/>                                                         |
| [**Publicação**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Define as propriedades de log para a sessão que o canal usa. Somente canais e canais de depuração e análise que usam o isolamento personalizado podem especificar propriedades de registro em log para sua sessão.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Type</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>string</td>
<td>Um <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">descritor de</a> acesso SDDL (Linguagem de Definição do Descritor de Segurança) que controla o acesso ao arquivo de log que faz o back-back do canal. Se o <strong>atributo de</strong> isolamento for definido como Aplicativo ou Sistema, o descritor de acesso controlará o acesso de leitura ao arquivo (as permissões de gravação serão ignoradas). Se o <strong>atributo de</strong> isolamento for definido como Personalizado, o descritor de acesso controlará o acesso de gravação ao canal e o acesso de leitura ao arquivo.<br/></td>
</tr>
<tr class="even">
<td>chid</td>
<td>token</td>
<td>Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa. Use esse valor ao referenciar o canal em um evento. Se você não especificar um identificador de canal, use o nome do canal para referenciar esse canal em uma definição de evento.<br/></td>
</tr>
<tr class="odd">
<td>Habilitado</td>
<td>booleano</td>
<td>Determina se o canal está habilitado. Definido como <strong>true para</strong> permitir o registro em log no canal; caso contrário, <strong>false.</strong> O padrão é <strong>false</strong> (o log está desabilitado).<br/> Como os tipos de canal de Depuração e Análise são canais de alto volume, você deve habilitar o canal somente ao investigar um problema com um componente que grava nesse canal; caso contrário, o canal deverá permanecer desabilitado.<br/> Cada vez que você habilita um canal de Depuração e Análise, o serviço limpa os eventos do canal.<br/></td>
</tr>
<tr class="even">
<td>isolamento</td>
<td>string</td>
<td>O valor de isolamento define as permissões de acesso padrão para o canal. É possível especificar um dos seguintes valores:
<ul>
<li><strong>Aplicativo</strong></li>
<li><strong>System</strong></li>
<li><strong>Personalizado</strong></li>
</ul>
O isolamento padrão é <strong>Application</strong>. As permissões padrão para Application <strong>são</strong> (mostradas usando SDDL): <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Texto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p>As permissões padrão para <strong>System são</strong> (mostradas usando SDDL):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Texto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>As permissões padrão para <strong>Isolamento</strong> personalizado são as mesmas que Application.</p>
<p>Os canais que <strong>especificam o isolamento</strong> do aplicativo usam a mesma sessão ETW. O mesmo é verdadeiro para o <strong>isolamento do</strong> sistema. No entanto, se você especificar <strong>Isolamento</strong> personalizado, o serviço criará uma sessão ETW separada para o canal. Usar <strong>o</strong> isolamento personalizado permite controlar as permissões de acesso para o canal e o arquivo de backing. Como há apenas 64 sessões ETW disponíveis, você deve limitar o uso do <strong>Isolamento</strong> personalizado.</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>string</td>
<td><p>O nome de exibição localizado para o canal. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> do manifesto.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>O nome do canal. O nome deve ser exclusivo na lista de canais que o provedor usa. A convenção para nomear canais é anexar o tipo de canal ao nome do provedor. Por exemplo. se o nome do provedor for Company-Product-Component e você estiver definindo um canal operacional, o nome será Company-Product-Component/Operational.</p>
<p>Os nomes de canal devem ter menos de 255 caracteres e não podem conter os seguintes caracteres: '>', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>O símbolo a ser usado para referenciar o canal em seu aplicativo. O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagem (MC.exe)</strong></a> usa o símbolo para criar uma constante para o canal no arquivo de header que o compilador gera. Se você não especificar um símbolo, o compilador gerará o nome para você.</p></td>
</tr>
<tr class="even">
<td>type</td>
<td>string</td>
<td><p>Identifica o tipo do canal. Você pode especificar um dos seguintes tipos:</p>
<ul>
<li><strong>Administrador</strong></li>
<li><strong>Operacional</strong></li>
<li><strong>Analítico</strong></li>
<li><strong>Depurar</strong></li>
</ul>
<p>Os canais de tipo de administrador suportam eventos destinados a usuários finais, administradores e pessoal de suporte. Os eventos gravados nos canais de administrador devem ter uma solução bem definida na qual o administrador pode agir. Um exemplo de evento de administrador é um evento que ocorre quando um aplicativo falha ao se conectar a uma impressora. Esses eventos são bem documentados ou têm uma mensagem associada a eles que fornece ao leitor instruções diretas sobre o que deve ser feito para corrigir o problema.</p>
<p>Os canais de tipo operacional suportam eventos que são usados para analisar e diagnosticar um problema ou ocorrência. Eles podem ser usados para disparar ferramentas ou tarefas com base no problema ou na ocorrência. Um exemplo de evento operacional é um evento que ocorre quando uma impressora é adicionada ou removida de um sistema.</p>
<p>Os canais de tipo de análise suportam eventos publicados em alto volume. Eles descrevem a operação do programa e indicam os problemas que não podem ser tratados por intervenção do usuário.</p>
<p>Os canais de tipo de depuração suportam eventos que são usados exclusivamente pelos desenvolvedores para diagnosticar um problema para depuração.</p>
<p>Os canais de análise e depuração são desabilitados por padrão e só devem ser habilitados para determinar a causa de um problema. Por exemplo, você habilitaria o canal, executaria o cenário que está causando o problema, desabilitaria o canal e, em seguida, consultaria os eventos. Observe que a habilitação do canal limpa o canal de eventos existentes. Se o canal de análise e depuração usar um arquivo de backing circular, você deverá desabilitar o canal para consultar seus eventos.</p>
<p>Todos os canais de administrador usam a mesma sessão ETW; o mesmo é verdadeiro para canais operacionais. No entanto, cada canal de análise e depuração usa uma sessão ETW separada, que é outro motivo para habilitar apenas esses tipos de canal quando necessário (há um número limitado de sessões ETW disponíveis).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Um identificador numérico que identifica exclusivamente o canal dentro da lista de canais que o provedor define. O compilador de mensagem atribuirá o valor se não for especificado.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

se o nome do canal seguir a convenção de nomenclatura de canal, o Windows Visualizador de Eventos listará o canal usando a cadeia de caracteres que segue a barra invertida. Por exemplo, se o nome do canal for empresa-produto-componente/operacional, a Visualizador de Eventos listará o canal como operacional no provedor da empresa-produto-componente. Caso contrário, o nome inteiro do canal será mostrado no provedor. O nome de exibição localizado é usado, se fornecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




`
