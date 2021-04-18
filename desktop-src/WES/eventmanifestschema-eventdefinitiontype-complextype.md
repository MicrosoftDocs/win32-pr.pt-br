---
title: Tipo complexo EventDefinitionType
description: Define um evento que seu provedor pode gravar.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Log de eventos do tipo complexo EventDefinitionType
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770541"
---
# <a name="eventdefinitiontype-complex-type"></a>Tipo complexo EventDefinitionType

Define um evento que seu provedor pode gravar.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

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
<td>channel</td>
<td>token</td>
<td>Um identificador que identifica o canal no qual o evento é gravado. Especifique um identificador de canal de um dos canais que você definiu ou importou. Se o canal não especificar um identificador de canal, use o nome do canal. Para obter detalhes sobre como definir ou importar um canal, consulte o tipo complexo <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .<br/> Se você não especificar um canal, o evento não será gravado em um canal. Normalmente, o único motivo para não especificar um canal é se você estiver gravando eventos somente em uma sessão do ETW. Para obter detalhes, consulte criando uma sessão do ETW, consulte <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controlando sessões de rastreamento de eventos</a>.<br/></td>
</tr>
<tr class="even">
<td>palavras-chave</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNamelist</strong></a></td>
<td>Uma lista separada por espaços de nomes de palavras-chave que identificam a categoria de eventos aos quais esse evento pertence. Especifique um nome de palavra-chave na lista de palavras-chave que você definir. Para obter detalhes sobre como definir palavras-chave, consulte o tipo complexo <a href="eventmanifestschema-keywordtype-complextype.md"><strong>keywordtype</strong></a> .<br/> Se você não especificar palavras-chave, o descritor de eventos conterá um zero para palavras-chave.<br/></td>
</tr>
<tr class="odd">
<td>nível</td>
<td><strong>QName</strong></td>
<td>O nível de detalhamento a ser usado ao gravar o evento. Especifique o nome de um nível que você definiu no manifesto ou um dos níveis definidos no arquivo de \Include\Winmeta.xml que está incluído no SDK do Windows. Para obter detalhes sobre como definir um nível, consulte o tipo complexo <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .<br/> Se você não especificar um nível, o descritor de eventos conterá um zero para o nível.<br/> Você deve especificar um nível se o tipo de canal para o qual o evento é gravado for admin; o nível deve ser um dos seguintes níveis definidos no Winmeata.xml:
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></td>
<td>A mensagem localizada para o evento. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> do manifesto.<br/> Você deverá especificar uma mensagem se o tipo de canal para o qual o evento é gravado for admin.<br/></td>
</tr>
<tr class="odd">
<td>Não registrado em log</td>
<td>booleano</td>
<td>Determina se o provedor registra esse evento. Especifique true se o provedor registrar esse evento; caso contrário, false. Use esse atributo para indicar que o provedor não está mais registrando esse evento em vez de remover o evento do manifesto. Manter o evento no manifesto permitirá que os consumidores decodifiquem arquivos ETL mais antigos que incluam o evento.<br/> <strong>Windows Server 2008 e Windows Vista:</strong> Não há suporte para esse atributo em versões do compilador de mensagens enviadas antes da versão do Windows 7 do SDK do Windows.<br/></td>
</tr>
<tr class="even">
<td>opcode</td>
<td><strong>QName</strong></td>
<td>O nome de um opcode que identifica uma operação dentro da tarefa. Especifique o nome de um opcode que você definiu no manifesto ou um dos opcodes definidos em Winmeta.xml. Para obter detalhes sobre como definir um opcode, consulte o tipo complexo <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpCodeType</strong></a> .<br/> Se a tarefa que você referencia contém opcodes específicos da tarefa (local), você pode especificar um de seus opcodes específicos da tarefa ou um opcode definido no nível do provedor (um opcode global). Se você especificar um opcode global, o valor do opcode global não poderá ser o mesmo que um dos opcodes locais para a tarefa.<br/> Se você fizer referência a um opcode local, o atributo Task deverá fazer referência à tarefa à qual o opcode local pertence.<br/> Se você não especificar um opcode, o descritor de eventos conterá um zero para opcode.<br/></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td>O símbolo a ser usado para referenciar o descritor de eventos para esse evento em seu aplicativo. O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagens (MC.exe)</strong></a> usa o símbolo para criar uma constante para o descritor de eventos no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você. Você usa o descritor ao chamar a função <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> para gravar o evento.<br/></td>
</tr>
<tr class="even">
<td>task</td>
<td><strong>QName</strong></td>
<td>O nome de uma tarefa que identifica o componente ou subcomponente que gera esse evento. Especifique o nome de uma tarefa que você definiu no manifesto. Para obter detalhes sobre como definir uma tarefa, consulte o tipo complexo <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .<br/> Se você não especificar uma tarefa, o descritor de eventos conterá um zero para a tarefa.<br/></td>
</tr>
<tr class="odd">
<td>template</td>
<td>token</td>
<td>O identificador de modelo do modelo que define os itens de dados que esse evento inclui. Especifique o identificador de um modelo que você definiu no manifesto. Para obter detalhes sobre como definir um modelo, consulte o tipo complexo <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>value</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32type</strong></a></td>
<td>O identificador de evento. O identificador deve ser exclusivo na lista de eventos que você definir.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Um número de versão de um byte da definição de evento.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Se você usar [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para formatar a cadeia de caracteres da mensagem para o evento (ou usar o Visualizador de eventos para exibir a cadeia de caracteres da mensagem), a cadeia de caracteres de mensagem poderá conter cadeias de inserção e qualquer uma das cadeias de caracteres de formato suportadas pela função **FormatMessage** do Win32. As cadeias de caracteres de inserção estão limitadas a%*n* ou%*n*! s! (por exemplo, %1) em que *n* é a referência baseada em um dos itens de dados definidos no modelo do evento. A cadeia de caracteres de mensagem também pode conter cadeias de inserção de parâmetro no formato%%*n* (por exemplo,% %4). O número máximo de cadeias de caracteres de inserção que a mensagem pode conter é 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

