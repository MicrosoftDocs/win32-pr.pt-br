---
title: Estrutura de RAS_PPP_ATCP_RESULT (Rassapi. h)
description: A estrutura de resultados do ATCP do RAS \_ PPP \_ \_ é usada para relatar o resultado de uma operação de projeção do protocolo AppleTalk para uma porta.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS da estrutura de RAS_PPP_ATCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918555"
---
# <a name="ras_ppp_atcp_result-structure"></a>\_Estrutura de \_ resultados do ATCP do RAS PPP \_

\[Não há suporte para a estrutura de **\_ resultados do \_ ATCP \_ do protocolo RAS** no Windows Vista.\]

A estrutura de **\_ resultados do \_ ATCP \_ do RAS PPP** é usada para relatar o resultado de uma operação de projeção do protocolo AppleTalk para uma porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwError**
</dt> <dd>

Especifica um valor que indica os resultados da operação de projeção do AppleTalk. Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido. Se a operação de projeção não for bem-sucedida, **dwError** será um código de erro de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o endereço IP atribuído ao cliente remoto.

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

[**\_resultado da \_ projeção do RAS PPP \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





