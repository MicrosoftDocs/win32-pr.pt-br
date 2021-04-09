---
description: Define os diferentes Estados de erro da extensão de origem de mídia.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Enumeração de MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091155"
---
# <a name="mf_mse_error-enumeration"></a>Enumeração de erros do MF \_ MSE \_

Define os diferentes Estados de erro da extensão de origem de mídia.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_ \_ erro \_ NOERROR do MF MSE**
</dt> <dd>

Não especifica nenhum erro.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**rede de erros do MF \_ MSE \_ \_**
</dt> <dd>

Especifica um erro com a rede.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**decodificação de \_ erro MF MSE \_ \_**
</dt> <dd>

Especifica um erro com decodificação.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**erro \_ \_ desconhecido de \_ erro \_ do MF MSE**
</dt> <dd>

Especifica um erro desconhecido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




