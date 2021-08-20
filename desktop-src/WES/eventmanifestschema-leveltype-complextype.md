---
title: Tipo complexo LevelType
description: Define um valor de severidade que determina o detalhado dos eventos que estão sendo registrados.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Tipo complexo LevelType EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b80e034f6b77f869207ecb785edbb935841eed2dba6bde73ad88c441dabf15cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055934"
---
# <a name="leveltype-complex-type"></a>Tipo complexo LevelType

Define um valor de severidade que determina o detalhado dos eventos que estão sendo registrados.

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome    | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para o nível. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**stringTable**](eventmanifestschema-stringtable-resources-element.md) do manifesto. <br/>                                                                                                    |
| name    | **QName**                                                         | O nome a ser atribuído a esse nível. Esse nome deve ser exclusivo dentro do escopo do provedor.<br/>                                                                                                                                                                                                            |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o nível em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o nível no arquivo de header que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |
| valor   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | O valor de nível. Você pode especificar valores no intervalo de 16 a 255. Para valores de nível predefinidos, consulte Comentários.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Comentários

A seguir estão os valores de nível predefinidos que você pode usar. Esses valores são definidos no arquivo Winmeta.xml que está incluído no SDK do Windows.



| Nome              | Valor | Símbolo                    | Descrição                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | NÍVEL DE \_ WINEVENT \_ CRÍTICO | Identifica um evento de saída ou encerramento anormal.<br/>            |
| win:Error         | 2     | ERRO DE \_ NÍVEL DE \_ WINEVENT    | Identifica um evento de erro grave.<br/>                             |
| win:Warning       | 3     | AVISO DE \_ NÍVEL DE \_ WINEVENT  | Identifica um evento de aviso, como uma falha de alocação.<br/>    |
| win:Informational | 4     | INFORMAÇÕES DE \_ NÍVEL DO \_ WINEVENT     | Identifica um evento sem erro, como um evento de entrada ou saída.<br/> |
| win:Verbose       | 5     | WINEVENT \_ LEVEL \_ VERBOSE  | Identifica um evento de rastreamento detalhado.<br/>                           |



 

Números mais altos implicam que você também tem níveis inferiores. Por exemplo, se você especificar win:Warning, receberá todos os avisos, erros e eventos críticos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





