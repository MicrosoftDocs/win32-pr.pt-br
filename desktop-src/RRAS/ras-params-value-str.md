---
title: RAS_PARAMS_VALUE união (Rassapi.h)
description: A união RAS PARAMS VALUE é usada na estrutura RAS PARAMETERS para armazenar os dados \_ \_ \_ associados a um parâmetro específico da mídia.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS RAS_PARAMS_VALUE união
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07453b707012c966fc298cc61973cb056b42d741d861a22204c17eec5265317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909596"
---
# <a name="ras_params_value-union"></a>União \_ de VALOR DO RAS PARAMS \_

\[A **\_ união RAS PARAMS \_ VALUE** não é suportada desde Windows Vista.\]

A **\_ união RAS PARAMS \_ VALUE** é usada na estrutura [**RAS \_ PARAMETERS**](ras-parameters-str.md) para armazenar os dados associados a um parâmetro específico da mídia. O **membro \_ tipo P** da estrutura **RAS \_ PARAMETERS** usa um valor da enumeração [**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md) para indicar o tipo de valor armazenado atualmente em **RAS \_ PARAMS \_ VALUE**.

## <a name="syntax"></a>Sintaxe


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Número**
</dt> <dd>

Se o **membro \_ P Type** da estrutura RAS [**\_ PARAMETERS**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico da mídia. Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.

Se o **membro \_ P Type** da estrutura RAS [**\_ PARAMETERS**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico da mídia. Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.

</dd> <dt>

**Cadeia de caracteres**
</dt> <dd>

Se o **membro \_ tipo P** da estrutura [**RAS \_ PARAMETERS**](ras-parameters-str.md) for ParamString, o membro **String** conterá o valor do parâmetro específico da mídia.

<dl> <dt>

**Comprimento**
</dt> <dd>

Especifica o comprimento, em caracteres, da cadeia de caracteres apontada pelo **membro** Data.

</dd> <dt>

**Dados**
</dt> <dd>

Ponteiro para um buffer que contém o valor da cadeia de caracteres de um parâmetro específico da mídia.

</dd> </dl> </dd> </dl>

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

[União de Administração de Servidor RAS](ras-server-administration-union.md)
</dt> <dt>

[**PARÂMETROS \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**FORMATO \_ RAS PARAMS \_**](ras-params-format-str.md)
</dt> </dl>

 

 





