---
description: Especifica permissões de controle de acesso para um arquivo em um cartão inteligente.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumeração de CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: e9a38e7d67e413352de693f52b07ba11bf34858854fa708b41a735152ad3ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771982"
---
# <a name="card_file_access_condition-enumeration"></a>\_Enumeração de \_ condição de acesso do arquivo de cartão \_

A **enumeração \_ \_ \_ condição de acesso ao arquivo do cartão** especifica permissões de controle de acesso para um arquivo em um [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Esse valor não é válido.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Todos podem ler o arquivo. Usuários específicos podem gravar no arquivo.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Somente usuários específicos podem ler ou gravar no arquivo.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Todos podem ler o arquivo. Os administradores podem gravar no arquivo.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

As permissões de acesso para o arquivo são desconhecidas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows xp, \[ somente aplicativos da área de trabalho do Windows xp\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows server 2003 \[ somente aplicativos da área de trabalho\]<br/>            |
| Cabeçalho<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de criptografia de cartão inteligente base da Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**\_informações do arquivo de cartão \_**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
