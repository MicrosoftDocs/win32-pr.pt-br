---
title: Função UtilStringCopyWithAlloc (Ndattributils.h)
description: Aloca e copia uma cadeia de caracteres de origem.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Função UtilStringCopyWithAlloc NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3654fa5eefd45a51d963325e10fbcba765420afe25a5c47a058bbaf4e4093ef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801526"
---
# <a name="utilstringcopywithalloc-function"></a>Função UtilStringCopyWithAlloc

A **função UtilStringCopyWithAlloc** aloca e copia uma cadeia de caracteres de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Buffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

O local em que o ponteiro para a memória alocada é armazenado. Quando não for mais necessário, ele deverá ser liberado com [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) Esse buffer é sempre terminado em nulo.

</dd> <dt>

*BufferMax* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O número máximo de caracteres a ler da *Origem.*

</dd> <dt>

*Origem* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

A cadeia de caracteres a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Os valores de retorno possíveis incluem, mas não estão limitados a, o seguinte.



| Código de retorno                                                                                  | Descrição                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi realizada com êxito.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros não foram fornecidos corretamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cotaskmemfree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

