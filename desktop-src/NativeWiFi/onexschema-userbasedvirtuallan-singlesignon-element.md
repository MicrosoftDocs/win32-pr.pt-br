---
description: Especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090662"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Elemento userBasedVirtualLan (logon único)

O elemento userBasedVirtualLan (logon único) especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário. Alguns dispositivos de NAS (servidor de acesso à rede) alteram a VLAN após a autenticação de um usuário. Quando userBasedVirtualLan for TRUE, o NAS poderá alterar a VLAN de um dispositivo após a autenticação de um usuário.

Esse elemento é opcional. Quando userBasedVirtualLan não é especificado em um perfil, um valor de FALSE é usado.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

O elemento **userBasedVirtualLan** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .

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

[**Logon único**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Logon único (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
