---
title: RAS_USER_0 estrutura (Rassapi.h)
description: A estrutura RAS USER 0 é usada nas funções \_ \_ RasAdminUserSetInfo e RasAdminUserGetInfo para especificar informações sobre um usuário.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- ras RAS_USER_0 estrutura de RAS_USER_0
- PRAS_USER_0 ras de estrutura
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789137"
---
# <a name="ras_user_0-structure"></a>Estrutura RAS \_ USER \_ 0

\[Esta versão da estrutura **RAS \_ USER \_ 0** não tem suporte desde o Windows Vista. Em vez disso, [**use o USUÁRIO RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) mais novo definido em mprapi.h.\]

A **estrutura RAS USER \_ \_ 0** é usada nas funções [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar informações sobre um usuário.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Membros

<dl> <dt>

**bfPrivilege**
</dt> <dd>

Um conjunto de sinalizadores de bits que especificam os privilégios RAS do usuário. Esse membro pode ser uma combinação do sinalizador RASPRIV \_ DialinPrivilege e um dos sinalizadores de retorno de chamada. Use a máscara RASPRIV \_ CallbackType para identificar o tipo de privilégio de retorno de chamada fornecido ao usuário. Os sinalizadores a seguir são definidos.



| Valor                                                                                                                                                                                                                                         | Significado                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ NoCallback**</dt> </dl>                             | O usuário não tem nenhum privilégio de retorno de chamada.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | A conta de usuário está configurada para que o administrador desfigura o número de retorno de chamada.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | O usuário remoto pode especificar um número de telefone de retorno de chamada ao discar.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | O usuário tem permissão para discar para esse servidor.<br/>                                 |



 

Especifique um dos sinalizadores de retorno de chamada na chamada para a [**função RasAdminUserSetInfo.**](rasadminusersetinfo.md)

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o número de telefone de retorno de chamada para o usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do RAS (Serviço de Acesso Remoto)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração de servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





