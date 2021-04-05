---
title: União de RAS_PARAMS_VALUE (Rassapi. h)
description: A \_ União de valor de params de Ras \_ é usada na estrutura de parâmetros de Ras \_ para armazenar os dados associados a um parâmetro específico de mídia.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS do RAS_PARAMS_VALUE Union
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
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085139"
---
# <a name="ras_params_value-union"></a>União de valor de \_ parâmetros RAS \_

\[A União de **\_ \_ valores de parâmetros RAS** não tem suporte a partir do Windows Vista.\]

A União de **\_ \_ valor de params de Ras** é usada na estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) para armazenar os dados associados a um parâmetro específico de mídia. O **membro \_ P Type** da estrutura de **\_ parâmetros de Ras** usa um valor da enumeração de [**\_ \_ formato de params de Ras**](ras-params-format-str.md) para indicar o tipo de valor atualmente armazenado no **\_ \_ valor de params RAS**.

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

Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico de mídia. Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.

Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico de mídia. Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.

</dd> <dt>

**Cadeia de caracteres**
</dt> <dd>

Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for Paramstring, o membro da **cadeia de caracteres** conterá o valor do parâmetro específico da mídia.

<dl> <dt>

**Comprimento**
</dt> <dd>

Especifica o comprimento, em caracteres, da cadeia de caracteres apontada pelo membro de **dados** .

</dd> <dt>

**Dados**
</dt> <dd>

Ponteiro para um buffer que contém o valor da cadeia de caracteres de um parâmetro específico de mídia.

</dd> </dl> </dd> </dl>

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

[Union de administração do servidor RAS](ras-server-administration-union.md)
</dt> <dt>

[**parâmetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**\_formato de parâmetros \_ RAS**](ras-params-format-str.md)
</dt> </dl>

 

 





