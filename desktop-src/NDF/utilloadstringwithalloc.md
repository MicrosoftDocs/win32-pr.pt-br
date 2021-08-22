---
title: Função UtilLoadStringWithAlloc (Ndattributils.h)
description: Aloca e carrega uma cadeia de caracteres da tabela de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Função UtilLoadStringWithAlloc NDF
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
ms.openlocfilehash: ca649599e2a8a29ecdab2dbbfe2c188947b40487ceb82ab4937622ce82c701a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685606"
---
# <a name="utilloadstringwithalloc-function"></a>Função UtilLoadStringWithAlloc

A **função UtilLoadStringWithAlloc** aloca e carrega uma cadeia de caracteres da tabela de recursos.

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

*uID* \[ Em\]
</dt> <dd>

Tipo: **UINT**

Identificador da cadeia de caracteres a ser carregada.

</dd> <dt>

*ppwzBuffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

O local em que a cadeia de caracteres recém-alocada será colocada. A cadeia de caracteres deve ser liberada [**usando CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando ela não for mais necessária.

</dd> <dt>

*cchBufferMax* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O número máximo de caracteres a carregar da tabela de recursos. Se a cadeia de caracteres de recurso for maior que o número de caracteres especificado, ela será truncada e terminada em nulo.

> [!Note]  
> Esse parâmetro pode não ser definido como zero.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**Cotaskmemfree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

