---
title: Tipo complexo ImportChannelType
description: Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Log de eventos do tipo complexo ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085517"
---
# <a name="importchanneltype-complex-type"></a>Tipo complexo ImportChannelType

Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chid   | token                                                             | Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa. Use esse valor ao referenciar esse canal em uma definição de evento. Se você não especificar um identificador de canal, use o nome do canal para fazer referência a esse canal em uma definição de evento.<br/>  |
| name   | anyURI                                                            | O nome do canal a ser importado.<br/>                                                                                                                                                                                                                                                                          |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o canal em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o canal no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |



## <a name="remarks"></a>Comentários

O manifesto que definiu o canal importado deve ser instalado antes que seu provedor grave eventos; caso contrário, os eventos não podem ser gravados no canal (a operação de gravação é realizada com sucesso, os eventos simplesmente não são gravados no canal).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





