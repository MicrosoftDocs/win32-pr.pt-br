---
title: Enumeração de WMDM_SESSION_TYPE
description: O \_ tipo de enumeração do tipo de sessão WMDM \_ define o tipo de sessão.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760479"
---
# <a name="wmdm_session_type-enumeration"></a>Enumeração de tipo de \_ sessão WMDM \_

O tipo de enumeração do **\_ \_ tipo de sessão WMDM** define o tipo de sessão.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**\_sessão WMDM \_ nenhum**
</dt> <dd>

A sessão não está definida.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_transferência de sessão do WMDM \_ para o \_ \_ dispositivo**
</dt> <dd>

A sessão é definida como transferindo dados para o dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transferência de sessão \_ do WMDM do \_ dispositivo**
</dt> <dd>

A sessão é definida como transferência de dados do dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_exclusão da sessão do WMDM \_**
</dt> <dd>

A sessão é definida como excluindo dados.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_sessão \_ personalizada do WMDM**
</dt> <dd>

A sessão é definida como uma sessão Personalizada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





