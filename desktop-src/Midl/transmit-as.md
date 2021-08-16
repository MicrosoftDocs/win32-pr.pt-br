---
title: Atributo transmit_as
description: O atributo \ transmitir \_ como \ instrui o compilador a associar o Type-ID, que é um tipo apresentado que os aplicativos cliente e servidor manipulam, com um tipo transmitido tipo de transmissão.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as do atributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382826"
---
# <a name="transmit_as-attribute"></a>transmitir \_ como atributo

O atributo **\[ transmitir \_ como \]** instrui o compilador a associar o **tipo ID**_,_ que é um tipo apresentado que os aplicativos cliente e servidor manipulam, com um tipo transmitido **tipo de transmissão.**

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de transmissão* 
</dt> <dd>

Especifica o tipo de dados que é transmitido entre o cliente e o servidor.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md), **\]** referência de atributo de ponteiro **\[** [](ref.md) **\]** , **\[** [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas. O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.

</dd> <dt>

*ID do tipo* 
</dt> <dd>

Especifica o nome do tipo de dados que é apresentado aos aplicativos cliente e servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar o atributo **\[ transmitir \_ como \]** , o usuário deve fornecer rotinas que convertam dados entre os tipos apresentados e transmitidos; essas rotinas também devem liberar memória usada para manter os dados convertidos. O atributo **\[ transmitir \_ como \]** instrui os stubs a chamar as rotinas de conversão fornecidas pelo usuário.

O tipo transmitido tipo *de transmissão* deve ser resolvido para um tipo base de MIDL, tipo predefinido ou um identificador de tipo. Para obter mais informações, consulte [tipos base de MIDL](midl-base-types.md).

O usuário deve fornecer as rotinas a seguir.



| Nome da rotina              | Descrição                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *tipo-ID * * * \_ para \_ transmissão**   | Converte dados do tipo apresentado para o tipo transmitido. Essa rotina aloca memória para o tipo transmitido e para todos os dados referenciados por ponteiros no tipo transmitido.                            |
| *tipo-ID * * * \_ da \_ transmissão** | Converte dados do tipo transmitido para o tipo apresentado. Essa rotina é responsável por alocar memória para dados referenciados por ponteiros no tipo apresentado. O RPC aloca memória para o próprio tipo. |
| *tipo-ID * * * \_ \_ InStr gratuito** | Libera memória alocada para dados referenciados por ponteiros no tipo apresentado. O RPC libera a memória para o próprio tipo.                                                                                               |
| *tipo-ID * * * \_ \_ transmissão gratuita** | Libera o armazenamento usado pelo chamador para o tipo transmitido e para os dados referenciados por ponteiros no tipo transmitido.                                                                                            |



 

 

O stub do cliente chama *Type-ID * * * \_ para \_ transmissão** para alocar espaço para o tipo transmitido e para converter os dados em objetos do tipo *transmissão-tipo.* O stub de servidor aloca espaço para o tipo de dados original e chama o *tipo de ID * * * \_ de \_ transmissão** para converter os dados de seu tipo transmitido para o tipo apresentado.

Após o retorno do código do aplicativo, o stub do servidor chama o *tipo-ID * * * \_ Free \_ Inst** para desalocar o armazenamento para o *tipo ID* no lado do servidor. O stub do cliente chama *Type-ID * * \_ * \_ transmissão gratuita** para desalocar o armazenamento do *tipo de transmissão* no lado do cliente.

Os tipos a seguir não podem ter um atributo de **\[ transmissão \_ as \]** :

-   Identificadores de contexto (tipos com o atributo de tipo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** e tipos que são usados como parâmetros com o atributo de **\[ \_ identificador \] de contexto** )
-   Tipos que são pipes ou derivados de pipes
-   Tipos de dados que são usados como o tipo base de uma definição de pipe
-   Parâmetros que são ponteiros ou resolvem para ponteiros
-   Parâmetros que são de conformidade, variáveis ou matrizes abertas
-   Estruturas que contêm matrizes de conformidade
-   O identificador de tipo predefinido [**\_ t**](handle-t.md), [**void**](void.md)

Os tipos transmitidos devem estar de acordo com as seguintes restrições:

-   Eles não devem ser ponteiros ou conter ponteiros.
-   Eles não devem ser pipes ou conter pipes.

## <a name="examples"></a>Exemplos

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**processamento**](handle.md)
</dt> <dt>

[**lidar com \_ t**](handle-t.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**livre**](void.md)
</dt> </dl>

 

 