---
description: Inicializa a \_ biblioteca Klib aux.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Função AuxKlibInitialize (aux \_ klib. h)
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
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747682"
---
# <a name="auxklibinitialize-function"></a>Função AuxKlibInitialize

Inicializa a \_ biblioteca Klib aux. Essa função deve ser chamada antes que qualquer outra função na biblioteca possa ser chamada.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.

Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus. h, que está disponível no WDK.

## <a name="remarks"></a>Comentários

A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de API auxiliar do Windows versão 1,0 ou posterior<br/>                            |
| parâmetro<br/>          | <dl> <dt>\_Klib aux. h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>\_Klib. lib do aux</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




