---
title: Tipo complexo EventDefinitionType
description: Define um evento que seu provedor pode gravar.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType tipo complexo EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42959edd4c7f7f49c3ced305b5b9bd1072f721a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482982"
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




| Nome | Type | Descrição | 
|------|------|-------------|
| channel | token | Um identificador que identifica o canal no qual o evento é gravado. Especifique um identificador de canal de um dos canais que você definiu ou importou. Se o canal não especificar um identificador de canal, use o nome do canal. Para obter detalhes sobre como definir ou importar um canal, consulte o tipo complexo <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType.</strong></a><br /> Se você não especificar um canal, o evento não será gravado em um canal. Normalmente, o único motivo para não especificar um canal é se você estiver escrevendo eventos somente em uma sessão ETW. Para obter detalhes, consulte Criando uma sessão ETW, consulte <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlando sessões de rastreamento de eventos</a>.<br /> | 
| palavras-chave | <a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a> | Uma lista separada por espaço de nomes de palavras-chave que identificam a categoria de eventos aos quais esse evento pertence. Especifique um nome de palavra-chave na lista de palavras-chave que você definir. Para obter detalhes sobre como definir palavras-chave, consulte o tipo <a href="eventmanifestschema-keywordtype-complextype.md"><strong>complexo KeywordType.</strong></a><br /> Se você não especificar palavras-chave, o descritor de evento conterá um zero para palavras-chave.<br /> | 
| nível | <strong>QName</strong> | O nível de detalhes a ser usado ao escrever o evento. Especifique o nome de um nível definido no manifesto ou um dos níveis definidos no arquivo \Include\Winmeta.xml que está incluído no SDK do Windows. Para obter detalhes sobre como definir um nível, consulte o <a href="eventmanifestschema-leveltype-complextype.md"><strong>tipo complexo LevelType.</strong></a><br /> Se você não especificar um nível, o descritor de evento conterá um zero para level.<br /> Você deve especificar um nível se o tipo de canal no qual o evento é gravado for Admin; O nível deve ser um dos seguintes níveis definidos em Winmeata.xml:<ul><li>win:Critical</li><li>win:Error</li><li>win:Warning</li><li>win:Informational</li></ul><br /> | 
| message | <a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a> | A mensagem localizada para o evento. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> do manifesto.<br /> Você deve especificar uma mensagem se o tipo de canal no qual o evento é gravado for Admin.<br /> | 
| notLogged | booleano | Determina se o provedor registra esse evento. Especifique true se o provedor registra esse evento; caso contrário, false. Use esse atributo para indicar que o provedor não está mais registrando esse evento em log em vez de remover o evento do manifesto. Manter o evento no manifesto permitirá que os consumidores decodificarem arquivos ETL mais antigos que incluem o evento.<br /><strong>Windows Server 2008 e Windows Vista:</strong> Esse atributo não tem suporte em versões do compilador de mensagem que foram enviadas antes da versão Windows 7 do SDK Windows.<br /> | 
| Opcode | <strong>QName</strong> | O nome de um opcode que identifica uma operação dentro da tarefa. Especifique o nome de um opcode que você definiu no manifesto ou um dos opcodes definidos Winmeta.xml. Para obter detalhes sobre como definir um opcode, consulte o <a href="eventmanifestschema-opcodetype-complextype.md"><strong>tipo complexo OpcodeType.</strong></a><br /> Se a tarefa referenciada contiver opcodes específicos da tarefa (local), você poderá especificar um de seus opcodes específicos da tarefa ou um opcode definido no nível do provedor (um opcode global). Se você especificar um opcode global, o valor do opcode global não poderá ser igual a um dos opcodes locais para a tarefa.<br /> Se você referenciar um opcode local, o atributo de tarefa deverá referenciar a tarefa à qual o opcode local pertence.<br /> Se você não especificar um opcode, o descritor de evento conterá um zero para opcode.<br /> | 
| símbolo | <a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a> | O símbolo a ser usado para referenciar o descritor de evento para esse evento em seu aplicativo. O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagem (MC.exe)</strong></a> usa o símbolo para criar uma constante para o descritor de evento no arquivo de header que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você. Você usa o descritor ao chamar a <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>função EventWrite</strong></a> para gravar o evento.<br /> | 
| task | <strong>QName</strong> | O nome de uma tarefa que identifica o componente ou o subcomponente que gera esse evento. Especifique o nome de uma tarefa que você definiu no manifesto. Para obter detalhes sobre como definir uma tarefa, consulte o <a href="eventmanifestschema-tasktype-complextype.md"><strong>tipo complexo TaskType.</strong></a><br /> Se você não especificar uma tarefa, o descritor de evento conterá um zero para a tarefa.<br /> | 
| template | token | O identificador de modelo do modelo que define os itens de dados que esse evento inclui. Especifique o identificador de um modelo que você definiu no manifesto. Para obter detalhes sobre como definir um modelo, consulte o <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>tipo complexo TemplateItemType.</strong></a><br /> | 
| value | <a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a> | O identificador de evento. O identificador deve ser exclusivo dentro da lista de eventos que você define.<br /> | 
| version | unsignedByte | Um número de versão de um byte da definição de evento.<br /> | 




## <a name="remarks"></a>Comentários

Se você usar [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para formatar a cadeia de caracteres de mensagem para o evento (ou usar o Visualizador de Eventos para exibir a cadeia de caracteres de mensagem), a cadeia de caracteres de mensagem poderá conter cadeias de caracteres de inserção e qualquer uma das cadeias de caracteres de formato compatíveis com a função **FormatMessage** win32. As cadeias de caracteres de inserção são limitadas a %*n* ou %*n*!s! (por exemplo, %1) em *que n* é a referência baseada em um dos itens de dados definidos no modelo do evento. A cadeia de caracteres de mensagem também pode conter cadeias de caracteres de inserção de parâmetro no formato %%*n* (por exemplo, %%4). O número máximo de cadeias de caracteres de inserção que a mensagem pode conter é 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

