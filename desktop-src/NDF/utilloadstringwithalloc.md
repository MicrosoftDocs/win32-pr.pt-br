---
title: Função UtilLoadStringWithAlloc (Ndattributils. h)
description: Aloca e carrega uma cadeia de caracteres da tabela de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- NDF da função UtilLoadStringWithAlloc
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086496"
---
# <a name="utilloadstringwithalloc-function"></a>Função UtilLoadStringWithAlloc

A função **UtilLoadStringWithAlloc** aloca e carrega uma cadeia de caracteres da tabela de recursos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UID* \[ no\]
</dt> <dd>

Tipo: **uint**

Identificador da cadeia de caracteres a ser carregada.

</dd> <dt>

*ppwzBuffer* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR \** _

O local onde a cadeia de caracteres alocada recentemente será colocada. A cadeia de caracteres deve ser liberada usando [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando não for mais necessária.

</dd> <dt>

*cchBufferMax* \[ no\]
</dt> <dd>

Tipo: **uint**

O número máximo de caracteres a serem carregados da tabela de recursos. Se a cadeia de caracteres do recurso for maior que o número de caracteres especificados, ela será truncada e terminada em nulo.

> [!Note]  
> Este parâmetro não pode ser definido como zero.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

