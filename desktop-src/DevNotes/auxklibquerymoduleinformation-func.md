---
description: Recupera informações sobre o conjunto de módulos carregado atualmente para o sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Função AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771687"
---
# <a name="auxklibquerymoduleinformation-function"></a>Função AuxKlibQueryModuleInformation

Recupera informações sobre o conjunto de módulos carregado atualmente para o sistema.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BufferSize* \[ entrada, saída\]
</dt> <dd>

Na entrada, o tamanho do buffer *QueryInfo* , em bytes. Na saída, recebe o tamanho real necessário. Como a lista de módulos do sistema pode ser alterada entre as chamadas, esse valor também pode ser alterado entre as chamadas.

</dd> <dt>

*Elementos de* \[ no\]
</dt> <dd>

O tamanho, em bytes, de um elemento de matriz. Esse tamanho determina o formato da saída.

</dd> <dt>

*QueryInfo* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe as informações do módulo. Essas informações são retornadas em uma matriz cujos elementos são uma das seguintes estruturas: [**informações \_ \_ básicas do \_ módulo aux**](aux-module-basic-info-struct.md) ou [**\_ \_ \_ informações estendidas do módulo aux**](aux-module-extended-info-struct.md). A estrutura específica usada depende do tamanho do elemento especificado.

Se esse parâmetro for **nulo**, a função retornará o tamanho de buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.

Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus. h, que está disponível no WDK.

## <a name="remarks"></a>Comentários

Você deve chamar a função [**AuxKlibInitialize**](auxklibinitialize-func.md) antes de chamar essa função.

A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de API auxiliar do Windows versão 1,0 ou posterior<br/>                            |
| parâmetro<br/>          | <dl> <dt>\_Klib aux. h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>\_Klib. lib do aux</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**\_ \_ informações básicas do módulo aux \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ informações estendidas do módulo aux \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




