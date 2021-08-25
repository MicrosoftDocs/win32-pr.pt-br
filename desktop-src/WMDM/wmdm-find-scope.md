---
title: WMDM_FIND_SCOPE enumeração
description: O tipo de \_ enumeração WMDM FIND \_ SCOPE define o escopo do objeto de armazenamento.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb7d4902b1acd4223f25bdc5e8a7ca76d4495b5f465687a56b295ad2d5fbfa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863006"
---
# <a name="wmdm_find_scope-enumeration"></a>Enumeração WMDM \_ FIND \_ SCOPE

O **tipo de \_ enumeração WMDM FIND \_ SCOPE** define o escopo do objeto de armazenamento.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ FIND \_ SCOPE \_ GLOBAL**
</dt> <dd>

Procurando o objeto correspondente em qualquer lugar do dispositivo.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**FILHOS IMEDIATOS DO ESCOPO DO WMDM \_ FIND \_ \_ \_**
</dt> <dd>

Procurando o objeto correspondente dentro desse armazenamento e seus filhos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





