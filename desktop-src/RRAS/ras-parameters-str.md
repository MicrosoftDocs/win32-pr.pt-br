---
title: RAS_PARAMETERS estrutura (Rassapi.h)
description: A estrutura RAS PARAMETERS é usada pela função RasAdminPortGetInfo para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um \_ servidor RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- ras RAS_PARAMETERS estrutura de RAS_PARAMETERS
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
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909666"
---
# <a name="ras_parameters-structure"></a>Estrutura \_ RAS PARAMETERS

\[Não há suporte para a estrutura **RAS \_ PARAMETERS** a partir Windows Vista.\]

A **estrutura \_ RAS PARAMETERS** é usada pela [**função RasAdminPortGetInfo**](rasadminportgetinfo.md) para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um servidor RAS.

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

**Chave \_ P**
</dt> <dd>

Especifica o nome da chave que representa o parâmetro específico da mídia, como MAXCONNECTBPS.

</dd> <dt>

**Tipo \_ P**
</dt> <dd>

Identifica o tipo de dados associados ao parâmetro . Esse membro pode ser um dos valores a seguir da [**enumeração RAS \_ PARAMS \_ FORMAT.**](ras-params-format-str.md)



| Valor                                                                                                                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica que os dados associados à chave são um número.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indica que os dados associados à chave são uma cadeia de caracteres.<br/> |



 

</dd> <dt>

**Atributos \_ P**
</dt> <dd>

Reservado.

</dd> <dt>

**Valor \_ P**
</dt> <dd>

Especifica o valor associado ao parâmetro . Esse membro é uma [**união RAS \_ PARAMS \_ VALUE.**](ras-params-value-str.md) Se o **membro \_ tipo P** for ParamNumber, o **membro Number** da união conterá o valor . Se **Tipo \_ P** for ParamString, o membro **String** da união conterá o valor .

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

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionConnectupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





