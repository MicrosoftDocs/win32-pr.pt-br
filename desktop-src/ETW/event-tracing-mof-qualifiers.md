---
description: Use os qualificadores definidos nesta seção ao criar sua classe MOF de provedor, classe MOF de evento, classe de tipo de evento MOF e as propriedades da classe MOF de tipo de evento.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Qualificadores MOF de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7b4250b73e84d46a19dab307d0c263ab1cc7782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837211"
---
# <a name="event-tracing-mof-qualifiers"></a>Qualificadores MOF de rastreamento de eventos

Use os qualificadores definidos nesta seção ao criar sua [classe MOF de provedor](#provider-mof-class-qualifiers), classe [MOF de evento](#event-mof-class-qualifiers), classe de [tipo de evento MOF](#event-type-mof-class-qualifiers)e [as propriedades da classe MOF de tipo de evento](#property-qualifiers). Para obter um exemplo que inclui alguns desses qualificadores, consulte [publicando seu esquema de evento](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>Qualificadores de classe MOF do provedor

A tabela a seguir lista os qualificadores que você pode especificar em uma classe MOF de provedor.



| Qualificador | Tipo de dados  | Descrição                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Volume**  | **Cadeia de caracteres** | Obrigatórios. GUID de cadeia de caracteres que identifica exclusivamente um provedor. Por exemplo, GUID ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Esse é o mesmo GUID que você usa ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar seu provedor. |



 

## <a name="event-mof-class-qualifiers"></a>Qualificadores de classe MOF de evento

A tabela a seguir lista os qualificadores que você pode especificar em uma classe de evento (a classe pai que agrupa as classes de tipo de evento relacionadas).

| Qualificador        | Tipo de dados   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Volume**         | **Cadeia de caracteres**  | Obrigatórios. GUID de cadeia de caracteres que identifica uma classe de eventos. Por exemplo, GUID ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Provedores de eventos usam o GUID para definir [**o \_ cabeçalho de rastreamento de eventos \_ . Membro GUID**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) , para que os consumidores possam determinar a classe de eventos que eles estão recebendo.                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **Inteiro** | Esse qualificador é opcional para a versão mais recente de uma classe de rastreamento de eventos e é necessário para todas as versões mais antigas da classe. A versão mais recente da classe não especifica o qualificador **EventVersion** ou tem o número de versão mais alto. Os números de versão começam com 0, por exemplo, EventVersion (0). Normalmente, quando você cria uma nova versão da classe, também renomeia a versão anterior para <classname> \_ VN, em que n é um número incremental que começa em 0. Para obter um exemplo, consulte [**FileIO**](fileio.md) e [**FileIO \_ V0**](fileio-v0.md).<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>Qualificadores de classe do tipo de evento MOF

A tabela a seguir lista os qualificadores que você pode especificar em uma classe de tipo de evento (a classe que define os dados de propriedade de evento).



| Qualificador         | Valor       | Descrição                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Inteiro** | Obrigatórios. Identifica a classe de tipo de evento. Por exemplo, EventType (1). O provedor de eventos usa o mesmo valor de tipo de evento para definir o [**cabeçalho de rastreamento de eventos \_ \_ . Classe. tipo**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Se a mesma classe MOF for usada para vários tipos de evento (porque eles usam os mesmos dados de evento), especifique o valor do tipo de evento como uma matriz de inteiros, por exemplo, EventType {12,15} . |
| **EventTypename** | **Cadeia de caracteres**  | Opcional. Descreve o tipo de evento. Por exemplo, EventTypename ("início"). Se a mesma classe MOF for usada para vários tipos de evento (porque eles usam os mesmos dados de evento), especifique o valor do nome do tipo de evento como uma matriz de cadeias de caracteres, por exemplo, EventTypename {"Start", "End"}. Os elementos da matriz EventTypename correspondem diretamente à matriz EventType.                 |



 

## <a name="property-qualifiers"></a>Qualificadores de propriedade

A tabela a seguir lista os qualificadores que você pode especificar em uma propriedade.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Qualificador</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BitMap</strong></td>
<td>Especifica as posições de bits que são mapeadas para valores de cadeia de caracteres. Se você especificar esse qualificador, também deverá especificar o qualificador <strong>Bitvalues</strong> .</td>
</tr>
<tr class="even">
<td><strong>Bitvalues</strong></td>
<td>Valores de cadeia de caracteres. Se o qualificador de <strong>bitmap</strong> também for especificado, as cadeias de caracteres corresponderão diretamente aos valores no qualificador de <strong>bitmap</strong> . Caso contrário, suponha que o valor da propriedade seja um índice baseado em um para as cadeias de caracteres de valor (o bit um corresponde à primeira cadeia de caracteres na lista).</td>
</tr>
<tr class="odd">
<td><strong>Extensão</strong></td>
<td>Fornece informações adicionais sobre como consumir (interpretar) os dados. O valor da extensão não diferencia maiúsculas de minúsculas. Inclua o valor entre aspas, por exemplo, extensão ( &quot; GUID &quot; ). Os valores de extensão possíveis são: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Volume</dt> <dd> Indica que os dados da propriedade são um GUID. O tipo de dados MOF deve ser <strong>Object</strong>. Espera-se que a carga seja uma estrutura de <strong>GUID</strong> .<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr e IPAddrV4</dt> <dd> Os dados são um endereço IP V4. O tipo de dados MOF deve ser <strong>Object</strong>. Espera-se que a carga seja um longo não assinado. Cada byte de longo sem sinal representa uma das quatro partes do endereço IP (P1. P2. P3. P4). O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.<br/> <strong>Antes do Windows Vista:</strong> Não há suporte para a extensão IPAddrV4.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Os dados são um endereço IP v6. O tipo de dados MOF deve ser <strong>Object</strong>. Espera-se que a carga seja uma estrutura de <strong>IN6_ADDR</strong> . <br/> <strong>Antes do Windows Vista:</strong> Não há suporte para a extensão IPAddrV6.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>Noprint</dt> <dd> Indica que o consumidor não deve imprimir esses dados.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</dt> <dd> Os dados identificam um número de porta. O tipo de dados MOF deve ser <strong>Object</strong>. Espera-se que a carga seja uma curta não assinada.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> Os caracteres de nova linha foram substituídos por espaços. Espera-se que a carga seja uma cadeia de caracteres ANSI terminada em nulo.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> Os caracteres de nova linha foram substituídos por espaços. Espera-se que a carga seja uma cadeia de caracteres largo, terminada em nulo.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>SIDs</dt> <dd> Os dados representam um SID de blob binário. O tipo de dados MOF deve ser <strong>Object</strong>. <br/> O SID é de um comprimento variável. O valor contido nos primeiros 4 bytes (<strong>ULONG</strong>) indica se o BLOB contém um Sid. Se os primeiros 4 bytes (<strong>ULONG</strong>) do blob forem diferentes de zero, o blob conterá um Sid. A primeira parte do BLOB contém a TOKEN_USER (a estrutura é alinhada em um limite de 8 bytes) e a segunda parte contém o SID. Para tratar da parte SID do blob:<br/>
<ul>
<li>Definir um ponteiro de byte para o início do blob</li>
<li>Multiplique o tamanho do ponteiro do log de eventos por 2 e adicione o produto ao ponteiro de byte ( <strong>o membro</strong> pointerize de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> contém o valor do tamanho do ponteiro)</li>
</ul>
<br/> Você pode usar a macro a seguir para determinar o comprimento do SID. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Indica que a propriedade contém um valor de ponteiro. O tamanho do valor do ponteiro depende do sistema operacional usado para registrar o evento; a carga conterá um valor de 4 bytes para sistemas de 32 bits ou um valor de 8 bytes para sistemas de 64 bits. O tipo de dados MOF deve ser <strong>Object</strong>.<br/> Os consumidores devem ignorar o tipo de dados e o qualificador de <strong>formato</strong> se a propriedade incluir a extensão de <strong>tamanho</strong> . Para determinar o tamanho dos dados a serem lidos para a propriedade, use:
<ul>
<li>O membro de <strong>ponteiros</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>O membro <strong>flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>Antes do Windows Vista:</strong> O valor de <strong>ponteiros</strong> pode não ser preciso. Por exemplo, em um computador de 64 bits, um aplicativo de 32 bits registrará ponteiros de 4 bytes; no entanto, a sessão definirá <strong>ponteiros</strong> para 8.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Variante</dt> <dd> Os dados representam um blob. Os primeiros quatro bytes (UInt32) indicam o tamanho do blob. O tipo de dados MOF deve ser <strong>Object</strong>. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> <dd> Traduz o carimbo de data/hora para a hora do sistema. O tipo de dados MOF deve ser <strong>Object</strong>. Espera-se que a carga seja um inteiro de 64 bits sem sinal.<br/> <strong>Antes do Windows Vista:</strong> Não disponível.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Formato</strong></td>
<td>Define o formato dos dados de propriedade. Por exemplo, incluindo o formato ( &quot; w &quot; ) em uma propriedade de cadeia de caracteres indica que a cadeia de caracteres é uma cadeia de caracteres larga. Os valores possíveis são:
<table>
<thead>
<tr class="header">
<th>Termo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>&<br/></td>
<td>Exiba o valor da propriedade como um caractere ASCII. Você pode usar esse qualificador com tipos de dados <strong>uint8</strong> .<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>&<br/></td>
<td>Trate a matriz de caracteres como uma cadeia de caracteres terminada em nulo. A cadeia de caracteres é uma cadeia de caracteres largo se o tipo de dados for <strong>char16</strong>; caso contrário, a cadeia de caracteres é uma cadeia de caracteres ASCII.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>Mostrar<br/></td>
<td>O valor da propriedade é uma cadeia de caracteres largos. Você pode usar esse qualificador com tipos de dados de <strong>cadeia de caracteres</strong> . <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>w.x.y.<br/></td>
<td>Exiba o valor da propriedade como um número hexadecimal. Você pode usar esse qualificador com tipos de dados inteiros de 16, 32-e de 64 bits.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Ponteiro</strong></td>
<td><p>Indica que a propriedade contém um valor de ponteiro. O tamanho do valor do ponteiro depende do sistema operacional usado para registrar o evento; a carga conterá um valor de 4 bytes para sistemas de 32 bits ou um valor de 8 bytes para sistemas de 64 bits. O tipo de dados MOF deve ser <strong>Object</strong>.</p>
<p>Os consumidores devem ignorar o tipo de dados e o qualificador de <strong>formato</strong> se a propriedade incluir a extensão de <strong>tamanho</strong> . Para determinar o tamanho dos dados a serem lidos para a propriedade, use:</p>
<ul>
<li>O membro de <strong>ponteiros</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>O membro <strong>flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>Antes do Windows Vista:</strong> O valor de <strong>ponteiros</strong> pode não ser preciso. Por exemplo, em um computador de 64 bits, um aplicativo de 32 bits registrará ponteiros de 4 bytes; no entanto, a sessão definirá <strong>ponteiros</strong> para 8.</p>
<p>Observe que alguns eventos usam <strong>ponteirotype</strong> em vez de <strong>ponteiro</strong>; Não use <strong>ponteirotype</strong>.</p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>Indica como a propriedade de cadeia de caracteres é encerrada. Por exemplo, StringTermination ( &quot; NullTerminated &quot; ) indica que a propriedade da cadeia de caracteres é terminada em nulo. Os valores possíveis são:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Consideradas</strong></dt> <dd>
<p>O comprimento da cadeia de caracteres é inserido no início da cadeia de caracteres como um valor <strong>UShort</strong> .</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>Não contado</strong></dt> <dd>
<p>A cadeia de caracteres não é terminada em nulo e o comprimento da cadeia de caracteres não é inserido no início da cadeia de caracteres. Nesse caso, a cadeia de caracteres deve ser o último elemento e ocupar todo o espaço até o final dos dados do evento.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>A cadeia de caracteres é terminada em nulo. Se você não especificar o qualificador <strong>StringTermination</strong> , a cadeia de caracteres será considerada como terminada em nulo.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>O comprimento da cadeia de caracteres é inserido no início da cadeia de caracteres como um valor <strong>UShort</strong> no formato big endian.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>Fornece descrições para cada valor no qualificador de <strong>valores</strong> . As funções <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> e <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> retornam essas descrições quando você tenta recuperar informações de nível e palavra-chave. As descrições são opcionais. Se você não fornecer as descrições, as funções retornarão <strong>nulas</strong>. Consulte <a href="#specifying-level-and-enable-flags-values-for-a-provider">especificando o nível e habilitar os valores de sinalizadores para um provedor</a> para obter mais detalhes.</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Especifica os valores de índice inteiro ou de sinalizador que são mapeados para valores de cadeia de caracteres. Se você especificar esse qualificador, também deverá especificar o qualificador de <strong>valores</strong> e, opcionalmente, o qualificador <strong>ValueType</strong> . Observe que o ETW não oferece suporte à opção WMI de ter cadeias de caracteres para valores de mapa de valor.
<p>O exemplo a seguir mostra como usar os qualificadores ValueMap, Values e ValueType.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Valores</strong></td>
<td>Valores de cadeia de caracteres. Se o qualificador de <strong>ValueMap</strong> também for especificado, as cadeias de caracteres corresponderão diretamente aos valores no qualificador <strong>ValueMap</strong> . Caso contrário, suponha que o valor da propriedade seja um índice de base zero nas cadeias de caracteres de valor.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Indica se os valores de <strong>ValueMap</strong> são valores de índice inteiro ou valores de sinalizador de bit. Se você não especificar esse qualificador, os valores de índice inteiro serão assumidos. Para especificar que os valores são valores de índice de inteiro, use ValueType ( &quot; index &quot; ). Para especificar que os valores são valores de sinalizador de bit, use ValueType ( &quot; Flag &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>Cada propriedade deve conter o qualificador <strong>WmiDataId</strong> . <strong>WmiDataId</strong> define a ordem na qual o consumidor lê os dados do evento. O valor de <strong>WmiDataId</strong> começa em 1 e é incrementado para cada propriedade na classe. Por exemplo, WmiDataId (1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Indica que os dados estão em formato XML e estão prontos para serem exibidos sem formatação adicional.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Especificando o nível e habilitam valores de sinalizadores para um provedor

Para documentar o nível e habilitar os sinalizadores que um controlador usaria para habilitar seu provedor, inclua as propriedades "Level" e "Flags" na classe MOF do provedor. Os nomes de propriedade de nível e sinalizadores diferenciam maiúsculas de minúsculas. As propriedades devem incluir os **valores** e qualificadores **ValueMap** , que especificam o nível possível e habilitam os valores de sinalizador. O **ValueMap** para os valores de sinalizador de habilitação deve ser valores bit (Flag). O qualificador **ValueDescriptions** é opcional, mas você deve usá-lo para fornecer descrições para cada valor possível. As descrições são usadas quando alguém chama as funções [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) e [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) para obter os valores de nível e habilitar sinalizadores (palavras-chave) possíveis para o provedor.

O seguinte mostra uma classe de provedor que especifica os valores de nível possível e habilitar sinalizadores.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
