---
title: Tipo complexo channelType
description: Define um canal para o qual os provedores podem registrar eventos.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- EventLog tipo complexo de channelType
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455622"
---
# <a name="channeltype-complex-type"></a>Tipo complexo channelType

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
| [**logout**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se o arquivo de log é sequencial ou circular.<br/>                                                         |
| [**editor**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Define as propriedades de log para a sessão que o canal usa. Somente canais de depuração e de análise e canais que usam o isolamento personalizado podem especificar propriedades de log para sua sessão.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>string</td>
<td>Um descritor de acesso SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">linguagem de definição de descritor de segurança</a> ) que controla o acesso ao arquivo de log que faz o backup do canal. Se o atributo de <strong>isolamento</strong> estiver definido como aplicativo ou sistema, o descritor de acesso controlará o acesso de leitura ao arquivo (as permissões de gravação serão ignoradas). Se o atributo de <strong>isolamento</strong> for definido como personalizado, o descritor de acesso controlará o acesso de gravação ao canal e o acesso de leitura ao arquivo.<br/></td>
</tr>
<tr class="even">
<td>chid</td>
<td>token</td>
<td>Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa. Use esse valor ao referenciar o canal em um evento. Se você não especificar um identificador de canal, use o nome do canal para fazer referência a esse canal em uma definição de evento.<br/></td>
</tr>
<tr class="odd">
<td>Habilitado</td>
<td>booleano</td>
<td>Determina se o canal está habilitado. Defina como <strong>true</strong> para permitir o registro em log do canal; caso contrário, <strong>false</strong>. O padrão é <strong>false</strong> (o registro em log está desabilitado).<br/> Como os tipos de canal de depuração e de análise são canais de alto volume, você deve habilitar o canal somente ao investigar um problema com um componente que grava nesse canal; caso contrário, o canal deve permanecer desabilitado.<br/> Cada vez que você habilita um canal de depuração e analítica, o serviço limpa os eventos do canal.<br/></td>
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
O isolamento padrão é <strong>aplicativo</strong>. As permissões padrão para o <strong>aplicativo</strong> são (mostradas usando SDDL): <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
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

<p>As permissões padrão para <strong>System</strong> são (mostradas usando SDDL):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<p>As permissões padrão para isolamento <strong>personalizado</strong> são as mesmas do aplicativo.</p>
<p>Os canais que especificam o isolamento de <strong>aplicativo</strong> usam a mesma sessão de ETW. O mesmo é verdadeiro para o isolamento do <strong>sistema</strong> . No entanto, se você especificar o isolamento <strong>personalizado</strong> , o serviço criará uma sessão ETW separada para o canal. Usar o isolamento <strong>personalizado</strong> permite controlar as permissões de acesso para o canal e o arquivo de backup. Como há apenas 64 sessões de ETW disponíveis, você deve limitar o uso de isolamento <strong>personalizado</strong> .</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>string</td>
<td><p>O nome de exibição localizado para o canal. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> do manifesto.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>O nome do canal. O nome deve ser exclusivo na lista de canais que o provedor usa. A Convenção de nomenclatura de canais é acrescentar o tipo de canal ao nome do provedor. Por exemplo. Se o nome do provedor for empresa-produto-componente e você estiver definindo um canal operacional, o nome será empresa-produto-componente/operacional.</p>
<p>Os nomes de canal devem ter menos de 255 caracteres e não podem conter os seguintes caracteres: ' > ', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>O símbolo a ser usado para referenciar o canal em seu aplicativo. O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagem (MC.exe)</strong></a> usa o símbolo para criar uma constante para o canal no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará o nome para você.</p></td>
</tr>
<tr class="even">
<td>tipo</td>
<td>string</td>
<td><p>Identifica o tipo do canal. Você pode especificar um dos seguintes tipos:</p>
<ul>
<li><strong>Administrador</strong></li>
<li><strong>Operacional</strong></li>
<li><strong>Analítico</strong></li>
<li><strong>Depurar</strong></li>
</ul>
<p>Os canais de tipo de administrador dão suporte a eventos que visam usuários finais, administradores e equipe de suporte. Os eventos gravados nos canais de administração devem ter uma solução bem definida na qual o administrador possa agir. Um exemplo de um evento de administrador é um evento que ocorre quando um aplicativo não consegue se conectar a uma impressora. Esses eventos são bem documentados ou têm uma mensagem associada a eles que fornecem instruções de leitura direta sobre o que deve ser feito para retificar o problema.</p>
<p>Os canais de tipo operacional dão suporte a eventos que são usados para analisar e diagnosticar um problema ou ocorrência. Eles podem ser usados para disparar ferramentas ou tarefas com base no problema ou na ocorrência. Um exemplo de evento operacional é um evento que ocorre quando uma impressora é adicionada ou removida de um sistema.</p>
<p>Os canais de tipo analítico dão suporte a eventos que são publicados em alto volume. Eles descrevem a operação do programa e indicam os problemas que não podem ser tratados por intervenção do usuário.</p>
<p>Os canais de tipo de depuração dão suporte a eventos que são usados exclusivamente por desenvolvedores para diagnosticar um problema de depuração.</p>
<p>Os canais analíticos e de depuração são desabilitados por padrão e só devem ser habilitados para determinar a causa de um problema. Por exemplo, você deve habilitar o canal, executar o cenário que está causando o problema, desabilitar o canal e, em seguida, consultar os eventos. Observe que a habilitação do canal limpa o canal de eventos existentes. Se o canal analítico e de depuração usar um arquivo de backup circular, você deverá desabilitar o canal para consultar seus eventos.</p>
<p>Todos os canais de administração usam a mesma sessão de ETW; o mesmo é verdadeiro para canais operacionais. No entanto, cada canal analítico e de depuração usa uma sessão ETW separada, que é outro motivo para habilitar esses tipos de canal apenas quando necessário (há um número limitado de sessões de ETW disponíveis).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Um identificador numérico que identifica exclusivamente o canal dentro da lista de canais que o provedor define. O compilador de mensagem atribui o valor, se não for especificado.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Se o nome do canal seguir a Convenção de nomenclatura de canal, o Visualizador de Eventos do Windows listará o canal usando a cadeia de caracteres que segue a barra invertida. Por exemplo, se o nome do canal for empresa-produto-componente/operacional, a Visualizador de Eventos listará o canal como operacional no provedor da empresa-produto-componente. Caso contrário, o nome inteiro do canal será mostrado no provedor. O nome de exibição localizado é usado, se fornecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




`
