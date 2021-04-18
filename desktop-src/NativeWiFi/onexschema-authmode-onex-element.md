---
description: Especifica o tipo de credenciais usadas para autenticação.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento AuthMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760233"
---
# <a name="authmode-onex-element"></a>Elemento AuthMode (OneX)

O elemento AuthMode (OneX) especifica o tipo de credenciais usadas para autenticação. A tabela a seguir descreve os valores possíveis.



| Valor         | Descrição                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | Use as credenciais do computador ou do usuário. Quando um usuário faz logon, as credenciais do usuário são usadas para autenticação. Quando nenhum usuário está conectado, as credenciais do computador são usadas. |
| computador       | Use somente as credenciais do computador.                                                                                                                                           |
| usuário          | Usar somente as credenciais do usuário.                                                                                                                                              |
| guest         | Use somente credenciais de convidado (vazias).                                                                                                                                     |



 

Esse elemento é opcional. Quando AuthMode não é especificado em um perfil, é usado um valor de `machineOrUser` .

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **AuthMode** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .

## <a name="remarks"></a>Comentários

Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** . Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 
