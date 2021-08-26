---
description: Recupera informações sobre o conjunto de módulos carregado no momento para o sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Função AuxKlibQueryModuleInformation (Aux \_ klib.h)
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
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045300"
---
# <a name="auxklibquerymoduleinformation-function"></a>Função AuxKlibQueryModuleInformation

Recupera informações sobre o conjunto de módulos carregado no momento para o sistema.

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

*BufferSize* \[ in, out\]
</dt> <dd>

Na entrada, o tamanho do buffer *QueryInfo,* em bytes. Na saída, recebe o tamanho real necessário. Como a lista de módulos do sistema pode mudar entre chamadas, esse valor também pode mudar entre chamadas.

</dd> <dt>

*ElementSize* \[ Em\]
</dt> <dd>

O tamanho, em bytes, de um elemento de matriz. Esse tamanho determina o formato da saída.

</dd> <dt>

*QueryInfo* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe as informações do módulo. Essas informações são retornadas em uma matriz cujos elementos são uma das seguintes estruturas: INFORMAÇÕES BÁSICAS DO MÓDULO AUX ou INFORMAÇÕES [**\_ ESTENDIDAS DO MÓDULO \_ \_ AUX**](aux-module-extended-info-struct.md). [**\_ \_ \_**](aux-module-basic-info-struct.md) A estrutura específica usada depende do tamanho do elemento especificado.

Se esse parâmetro for **NULL,** a função retornará o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será STATUS \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus.h, que está disponível no WDK.

## <a name="remarks"></a>Comentários

Você deve chamar [**a função AuxKlibInitialize**](auxklibinitialize-func.md) antes de chamar essa função.

A biblioteca de objetos que implementa essa API pode ser baixada [aqui.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de API auxiliar versão 1.0 ou posterior<br/>                            |
| Cabeçalho<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>Aux \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**INFORMAÇÕES \_ BÁSICAS DO MÓDULO AUX \_ \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**INFORMAÇÕES \_ ESTENDIDAS DO MÓDULO AUX \_ \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




