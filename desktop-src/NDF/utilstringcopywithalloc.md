---
title: Função UtilStringCopyWithAlloc (Ndattributils. h)
description: Aloca e copia uma cadeia de caracteres de origem.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- NDF da função UtilStringCopyWithAlloc
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
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789750"
---
# <a name="utilstringcopywithalloc-function"></a>Função UtilStringCopyWithAlloc

A função **UtilStringCopyWithAlloc** aloca e copia uma cadeia de caracteres de origem.

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

*Buffer* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR \** _

O local onde o ponteiro para a memória alocada é armazenado. Quando não for mais necessário, ele deve ser liberado com [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree). Esse buffer é sempre terminado em nulo.

</dd> <dt>

*BufferMax* \[ no\]
</dt> <dd>

Tipo: **uint**

O número máximo de caracteres a serem lidos da *origem*.

</dd> <dt>

*Origem* \[ do no\]
</dt> <dd>

Tipo: **LPCWSTR**

A cadeia de caracteres a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código de retorno                                                                                  | Descrição                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi realizada com êxito.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros não foram fornecidos corretamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

