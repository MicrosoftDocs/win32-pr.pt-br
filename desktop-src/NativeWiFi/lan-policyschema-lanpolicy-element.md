---
description: Contém uma política de LAN com fio.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811081"
---
# <a name="lanpolicy-element"></a>Elemento LANPolicy

O elemento LANPolicy contém uma política de LAN com fio. Esse é o elemento raiz exclusivo para um perfil de diretiva de rede com fio.

O namespace de destino para o elemento **LANPolicy** é `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                     | Descrição                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ndescrição**](lan-policyschema-description-lanpolicy-element.md)             | [**nometype**](lan-policyschema-nametype-simpletype.md) | Contém a descrição de uma política de LAN com fio. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | booleano                                                  | Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).<br/> |
| [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Contém as configurações globais para a configuração automática de redes com fio. <br/>                                                                                          |
| [**nomes**](lan-policyschema-name-lanpolicy-element.md)                           | [**nometype**](lan-policyschema-nametype-simpletype.md) | Contém o nome de uma política de LAN com fio. <br/>                                                                                                                                 |
| [**ProfileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Contém uma lista de perfis a serem aplicados no nível de domínio ou computador. <br/>                                                                                                |



## <a name="remarks"></a>Comentários

Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema de política de LAN](lan-policyschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




