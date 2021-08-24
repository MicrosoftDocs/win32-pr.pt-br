---
description: Inicializa a biblioteca Aux \_ klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Função AuxKlibInitialize (Aux \_ klib.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654876"
---
# <a name="auxklibinitialize-function"></a>Função AuxKlibInitialize

Inicializa a biblioteca Aux \_ klib. Essa função deve ser chamada antes que qualquer outra função na biblioteca possa ser chamada.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será STATUS \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus.h, que está disponível no WDK.

## <a name="remarks"></a>Comentários

A biblioteca de objetos que implementa essa API pode ser baixada [aqui.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de API auxiliar versão 1.0 ou posterior<br/>                            |
| Cabeçalho<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>Aux \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




