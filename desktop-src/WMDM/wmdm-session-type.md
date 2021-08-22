---
title: WMDM_SESSION_TYPE enumeração
description: O tipo de \_ enumeração TIPO \_ DE SESSÃO WMDM define o tipo de sessão.
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
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055524"
---
# <a name="wmdm_session_type-enumeration"></a>Enumeração TIPO \_ DE SESSÃO DO WMDM \_

O **tipo de \_ enumeração TIPO DE SESSÃO \_ WMDM** define o tipo de sessão.

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

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**SESSÃO WMDM \_ \_ NONE**
</dt> <dd>

A sessão não está definida.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**TRANSFERÊNCIA DE SESSÃO DO WMDM \_ \_ PARA O \_ \_ DISPOSITIVO**
</dt> <dd>

A sessão é definida como transferindo dados para o dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**TRANSFERÊNCIA DE SESSÃO DO WMDM \_ \_ DO \_ \_ DISPOSITIVO**
</dt> <dd>

A sessão é definida como transferindo dados do dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**EXCLUSÃO DE SESSÃO DO WMDM \_ \_**
</dt> <dd>

A sessão é definida como excluindo dados.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM \_ SESSION \_ CUSTOM**
</dt> <dd>

A sessão é definida como uma sessão personalizada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





