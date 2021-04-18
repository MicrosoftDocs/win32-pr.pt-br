---
title: Palavra-chave declare_guid
description: A \_ palavra-chave declare GUID instrui o MIDL a emitir uma variável GUID para o arquivo de cabeçalho gerado.
keywords:
- MIDL de palavra-chave declare_guid
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105764347"
---
# <a name="declare_guid-keyword"></a>\_palavra-chave de GUID declare

A palavra-chave **Declare \_ GUID** instrui o MIDL a emitir uma variável GUID para o arquivo de cabeçalho gerado.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da variável* 
</dt> <dd>

Especifica um nome de variável para o identificador no arquivo de cabeçalho gerado.

</dd> <dt>

*guid*
</dt> <dd>

Especifica o [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) que será aplicado ao nome da variável no arquivo de cabeçalho gerado.

</dd> </dl>

## <a name="examples"></a>Exemplos

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Comentários

O uso `declare_guid` do é equivalente ao uso `cpp_quote` do para gerar uma invocação da `EXTERN_GUID` macro.

O exemplo acima resulta na seguinte saída:

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

A `declare_guid` instrução é fornecida como uma conveniência. Ele tem a vantagem de usar a mesma sintaxe de GUID que o [ `uuid` atributo](uuid.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**atributo uuid**](uuid.md)
</dt> <dt>

[**Estrutura de GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
