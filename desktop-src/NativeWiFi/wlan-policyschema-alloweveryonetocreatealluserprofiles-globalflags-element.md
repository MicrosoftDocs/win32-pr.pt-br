---
description: Especifica se qualquer usuário pode criar um perfil de todos os usuários.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501560"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)

O elemento **allowEveryoneToCreateAllUserProfiles** (globalFlags) especifica se qualquer usuário pode criar um perfil de todos os usuários. Um perfil de todos os usuários pode ser usado por qualquer usuário no computador para se conectar à rede sem fio associada ao perfil.

Se **allowEveryoneToCreateAllUserProfiles** for true, qualquer usuário poderá criar um perfil de todos os usuários. Se **allowEveryoneToCreateAllUserProfiles** for false, nem todos os usuários poderão criar um perfil de todos-usuários e haverá uma DACL associada ao \_ objeto de segurança WLAN Secure \_ Adicionar \_ novo \_ todos os \_ \_ perfis de usuário que especifica os usuários ou grupos de usuário com permissão para criar perfis de todos os usuários. A DACL padrão especifica que somente os usuários que fizeram logon como um membro do grupo Administradores podem criar um perfil de todos os usuários. As configurações de segurança padrão podem ser alteradas chamando [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings). Para obter as configurações de segurança atuais, chame [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Esse elemento é obrigatório. Quando um perfil é criado pelo serviço de configuração automática, esse elemento terá o valor padrão de TRUE.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

O elemento **allowEveryoneToCreateAllUserProfiles** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




