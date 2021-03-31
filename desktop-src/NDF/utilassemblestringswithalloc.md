---
title: Função UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Aloca uma cadeia de caracteres e formata-a usando cadeias de caracteres fornecidas pela tabela de cadeias. Essa função usa StringCchPrintf para criar a cadeia de caracteres formatada.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- NDF da função UtilAssembleStringsWithAlloc
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645245"
---
# <a name="utilassemblestringswithalloc-function"></a>Função UtilAssembleStringsWithAlloc

A função **UtilAssembleStringsWithAlloc** aloca uma cadeia de caracteres e formata-a usando cadeias de caracteres fornecidas pela tabela de cadeias. Essa função usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) para criar a cadeia de caracteres formatada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Buffer* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR \** _

O local onde a cadeia de caracteres alocada recentemente será colocada. Quando a cadeia de caracteres não for mais necessária, ela deverá ser liberada com [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*BufferMax* \[ no\]
</dt> <dd>

Tipo: **uint**

O número máximo de caracteres permitidos na cadeia de caracteres alocada pelo *buffer*. Se a cadeia de caracteres formatada resultante for maior que o número de caracteres especificados, ela será truncada e terminada em nulo.

> [!Note]  
> Este parâmetro não pode ser definido como zero.

 

</dd> <dt>

*InputFormat* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadeia de caracteres fora da tabela de cadeia de caracteres que representa um parâmetro de formato passado para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Ele é construído usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

O formato da cadeia de caracteres do recurso deve especificar um parâmetro de formato que assume uma cadeia de caracteres larga ou um parâmetro de formato que leva uma cadeia de caracteres longa e não assinada.

</dd> <dt>

*Entradastring* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadeia de caracteres fora da tabela de cadeia de caracteres que representa um argumento passado para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) no lugar da cadeia de caracteres larga no parâmetro format. Ele é construído usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*AdditionalArgument* \[ no\]
</dt> <dd>

Tipo: **booliano**

True se *adicionalvalue* deve ser passado como o primeiro argumento de formatação para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); caso contrário, false (e somente a cadeia de caracteres de recurso identificada por *InputString* será passada).

</dd> <dt>

*Adicionalvalue* \[ no\]
</dt> <dd>

Tipo: **ULONG**

O valor a ser passado como o primeiro argumento de formatação para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) se *AdditionalArgument* for true.

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

