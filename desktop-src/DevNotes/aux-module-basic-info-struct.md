---
description: Contém informações básicas do módulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Estrutura de AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956145"
---
# <a name="aux_module_basic_info-structure"></a>\_Estrutura de \_ informações básicas do módulo aux \_

Contém informações básicas do módulo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**ImageBase**
</dt> <dd>

O endereço base do módulo dentro do espaço de endereço do kernel.

</dd> </dl>

## <a name="remarks"></a>Comentários

A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de API auxiliar versão 1,0 ou posterior<br/>                          |
| Cabeçalho<br/>          | <dl> <dt>\_Klib aux. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




