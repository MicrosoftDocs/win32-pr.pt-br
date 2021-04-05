---
title: atributo typedef
description: A palavra-chave de typedef IDL permite declarações de TypeDef que são muito semelhantes às declarações de typedef de linguagem C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- atributo de typedef MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640560"
---
# <a name="typedef-attribute"></a>atributo typedef

A palavra-chave de **TYPEDEF** IDL permite declarações de **typedef** que são muito semelhantes às declarações de **typedef** de linguagem C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IDL-tipo-atributo-List* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos em um arquivo IDL incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*. A palavra-chave [**const**](const.md) pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica declaradores de MIDL padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.

</dd> <dt>

*ACF-tipo-atributo-List* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos em um ACF incluem **\[** [**alocar**](allocate.md) **\]** , **\[** [**codificar**](encode.md) **\]** e **\[** [**decodificar**](decode.md) **\]** .

</dd> <dt>

*TypeName* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

A declaração de **typedef** de IDL é aumentada para permitir que você associe atributos de tipo aos tipos definidos. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .

A palavra-chave **typedef** em um ACF aplica atributos a tipos que são definidos no arquivo IDL correspondente. Por exemplo, o atributo [**alocar**](allocate.md) tipo permite que você personalize a alocação de memória e a desalocação pelo aplicativo e pelos stubs.

A instrução de **typedef** de ACF aparece como parte do corpo de ACF. Observe que a sintaxe de **typedef** de ACF é diferente da sintaxe de **typedef** de IDL e da sintaxe de **typedef** de linguagem C. Nenhum tipo novo pode ser introduzido no ACF.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**RET**](decode.md)
</dt> <dt>

[**codificado**](encode.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**processamento**](handle.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 