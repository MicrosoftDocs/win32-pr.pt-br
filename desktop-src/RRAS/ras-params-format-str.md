---
title: Enumeração de RAS_PARAMS_FORMAT (Rassapi. h)
description: O \_ tipo de enumeração de formato RAS params \_ é usado na \_ estrutura de parâmetros de RAS para indicar o tipo de dados associado a uma chave específica de mídia.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS de enumeração de RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673176"
---
# <a name="ras_params_format-enumeration"></a>Enumeração de formato de \_ parâmetros RAS \_

\[a enumeração de **\_ \_ formato de parâmetros RAS** não tem suporte a partir do Windows Vista.\]

O tipo de enumeração de **\_ \_ formato RAS params** é usado na estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) para indicar o tipo de dados associado a uma chave específica de mídia.

## <a name="syntax"></a>Syntax


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
</dt> <dd>

Indica que os dados associados à chave são um número.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**Paramstring**
</dt> <dd>

Indica que os dados associados à chave são uma cadeia de caracteres.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Enumerações de administração do servidor RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**parâmetros de RAS \_**](ras-parameters-str.md)
</dt> </dl>

 

 





