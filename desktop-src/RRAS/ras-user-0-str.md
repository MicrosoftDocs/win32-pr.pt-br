---
title: Estrutura de RAS_USER_0 (Rassapi. h)
description: A \_ estrutura do usuário 0 do RAS \_ é usada nas funções RasAdminUserSetInfo e RasAdminUserGetInfo para especificar informações sobre um usuário.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS da estrutura de RAS_USER_0
- RAS de ponteiro de estrutura de PRAS_USER_0
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
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499354"
---
# <a name="ras_user_0-structure"></a>\_Estrutura do usuário 0 do RAS \_

\[Esta versão da estrutura **do \_ usuário \_ do RAS 0** não tem suporte a partir do Windows Vista. Use o [**usuário RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) mais recente definido em mprapi. h em vez disso.\]

A estrutura do **\_ usuário \_ 0 do RAS** é usada nas funções [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar informações sobre um usuário.

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

Um conjunto de sinalizadores de bits que especificam os privilégios de RAS do usuário. Esse membro pode ser uma combinação do sinalizador RASPRIV \_ DialinPrivilege e um dos sinalizadores de retorno de chamada. Use a \_ máscara de retorno de chamada RASPRIV para identificar o tipo de privilégio de recall fornecido ao usuário. Os sinalizadores a seguir são definidos.



| Valor                                                                                                                                                                                                                                         | Significado                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ Nocallback**</dt> </dl>                             | O usuário não tem nenhum privilégio de retorno de chamada.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | A conta de usuário é configurada para que o administrador defina o número de retorno de chamada.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | O usuário remoto pode especificar um número de telefone de retorno ao discar no.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | O usuário tem permissão para fazer a conexão com este servidor.<br/>                                 |



 

Especifique um dos sinalizadores de retorno de chamada na chamada para a função [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o número de telefone de retorno para o usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração do servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





