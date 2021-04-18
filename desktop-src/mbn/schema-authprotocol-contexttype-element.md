---
description: Especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784122"
---
# <a name="authprotocol-contexttype-element"></a>Elemento AuthProtocol (contextType)

O elemento **AuthProtocol (ContextType)** especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).

O elemento pode ter um dos valores a seguir.

| Valor      | Significado                                                                 |
|------------|-------------------------------------------------------------------------|
| None     | Nenhum protocolo de autenticação.                                             |
| PAP      | Autenticação de senha não criptografada.                                    |
| VIA     | CHAP (Challenge Handshake Authentication Protocol).                      |
|  MsCHAPV2 | Use o protocolo CHAP (Microsoft s Challenge Handshake Authentication Protocol) v 2.0. |



 

Esse elemento é opcional e é usado somente para perfis GSM. Se o elemento não for especificado e o perfil for para um dispositivo GSM, o serviço de banda larga móvel usará **"nenhum"**.

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **AuthProtocol** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




