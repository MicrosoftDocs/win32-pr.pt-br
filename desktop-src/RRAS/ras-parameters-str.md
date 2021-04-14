---
title: Estrutura de RAS_PARAMETERS (Rassapi. h)
description: A estrutura de parâmetros de RAS \_ é usada pela função RasAdminPortGetInfo para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um servidor RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS da estrutura de RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499622"
---
# <a name="ras_parameters-structure"></a>Estrutura de parâmetros de RAS \_

\[A estrutura de **\_ parâmetros de Ras** não tem suporte no Windows Vista.\]

A estrutura de **\_ parâmetros de Ras** é usada pela função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um servidor RAS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Tecla P**
</dt> <dd>

Especifica o nome da chave que representa o parâmetro específico de mídia, como MAXCONNECTBPS.

</dd> <dt>

**Tipo de P \_**
</dt> <dd>

Identifica o tipo de dados associado ao parâmetro. Esse membro pode ser um dos seguintes valores da enumeração de [**\_ \_ formato de parâmetros de Ras**](ras-params-format-str.md) .



| Valor                                                                                                                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica que os dados associados à chave são um número.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**Paramstring**</dt> </dl> | Indica que os dados associados à chave são uma cadeia de caracteres.<br/> |



 

</dd> <dt>

**Atributos de P \_**
</dt> <dd>

Reservado.

</dd> <dt>

**\_Valor P**
</dt> <dd>

Especifica o valor associado ao parâmetro. Esse membro é uma União de [**\_ \_ valor de parâmetros RAS**](ras-params-value-str.md) . Se o membro do **\_ tipo P** for ParamNumber, o membro **Number** da União conterá o valor. Se **P \_ Type** for paramstring, o membro **String** da União conterá o valor.

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

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





