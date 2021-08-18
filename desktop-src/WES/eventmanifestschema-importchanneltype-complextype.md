---
title: Tipo complexo ImportChannelType
description: Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Tipo complexo ImportChannelType EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66136ee767c16aa85bfcef33fd23d5d42817f844fc309f7633d2a3d2bd35f2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471046"
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
| chid   | token                                                             | Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa. Use esse valor ao referenciar esse canal em uma definição de evento. Se você não especificar um identificador de canal, use o nome do canal para referenciar esse canal em uma definição de evento.<br/>  |
| name   | anyURI                                                            | O nome do canal a ser importado.<br/>                                                                                                                                                                                                                                                                          |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o canal em seu aplicativo. O [**MC.exe (Compilador de Mensagens)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o canal no arquivo de header que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |



## <a name="remarks"></a>Comentários

O manifesto que definiu o canal importado deve ser instalado antes que seu provedor escreva eventos; caso contrário, os eventos não podem ser gravados no canal (a operação de gravação é bem-sucedida, os eventos simplesmente não são gravados no canal).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





