---
title: context_handle atributo
description: O atributo \ do manipulador de contexto \_ \ identifica um identificador de associação que mantém o contexto, ou informações de estado, no servidor entre chamadas de procedimento remoto.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle do atributo MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640514"
---
# <a name="context_handle-attribute"></a>atributo de identificador de contexto \_

O atributo **\[ \_ identificador \] de contexto** identifica um identificador de associação que mantém o contexto, ou informações de estado, no servidor entre chamadas de procedimento remoto.

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de ponteiro ou um identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador e Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. O declarador para um identificador de contexto deve incluir pelo menos um Declarador de ponteiro. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas. O identificador de nome de parâmetro no Declarador de função é opcional.

</dd> <dt>

*função-attr-lista* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[ \_ identificador \] de contexto**.

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do **\*** designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado. Separe vários atributos com vírgulas.

</dd> <dt>

*tipo de identificador de contexto* 
</dt> <dd>

Especifica o identificador que especifica o tipo de identificador de contexto, conforme definido em uma declaração de [**typedef**](typedef.md) que usa o atributo de **\[ \_ identificador \] de contexto** . A rotina de encerramento é opcional.

**Windows Server ServerÂ 2003 e WINDOWSÂ XP:** Uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado). Esses recursos de acesso são comparáveis a mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores). Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados. Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados. Observe que os métodos de criação são serializados implicitamente.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo de **\[ \_ identificador \] de contexto** pode aparecer como um atributo de tipo de [**typedef**](typedef.md) de IDL, como um atributo de tipo de retorno de função ou como um atributo de parâmetro. Quando você aplica o atributo de **\[ \_ identificador \] de contexto** a uma definição de tipo, você também deve fornecer uma rotina de encerramento de contexto. Consulte [rotina de execução de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine) para obter detalhes.

Quando você usa o compilador MIDL no modo padrão ([**/MS \_ ext**](-ms-ext.md)), um identificador de contexto pode ser qualquer tipo de ponteiro selecionado pelo usuário, desde que ele esteja em conformidade com os requisitos para identificadores de contexto descritos aqui. Os dados associados a esse tipo de identificador de contexto não são transmitidos na rede e só devem ser manipulados pelo aplicativo de servidor. Os compiladores de IDL do DCE restringem identificadores de contexto a ponteiros do tipo [**void**](void.md) **\*** . Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.

Assim como ocorre com outros tipos de identificador, o identificador de contexto é opaco para o aplicativo cliente e todos os dados associados a ele não são transmitidos. No servidor, o identificador de contexto serve como um identificador no contexto ativo, e todos os dados associados ao tipo de identificador de contexto podem ser acessados.

Para criar um identificador de contexto, o cliente passa para o servidor um **\[** [](out-idl.md) **\]** ponteiro out, **\[** [**ref**](ref.md) **\]** para um identificador de contexto. (O próprio identificador de contexto pode ter um valor **nulo** ou não **nulo** — contanto que seu valor seja consistente com seus atributos de ponteiro. Por exemplo, quando o tipo de identificador de contexto tem o **\[** [](ref.md) **\]** atributo ref aplicado a ele, ele não pode ter um valor **nulo** .) Outro identificador de associação deve ser fornecido para realizar a associação até que o identificador de contexto seja criado. Quando nenhum identificador explícito é especificado, a associação implícita é usada. Quando nenhum **\[** atributo de [**\_ identificador implícito**](implicit-handle.md) **\]** está presente, um identificador automático é usado.

O procedimento remoto no servidor cria um identificador de contexto ativo. O cliente deve usar esse identificador de contexto como um **\[** [](in.md) **\]** parâmetro in ou **\[ in**, **out \]** em chamadas subsequentes. Um identificador de contexto somente **\[ \] no** pode ser usado como um identificador de associação, portanto, ele deve ter um valor não **nulo** . Um identificador de contexto somente **\[ no \]** não reflete as alterações de estado no servidor.

No servidor, o procedimento chamado pode interpretar o identificador de contexto conforme necessário. Por exemplo, o procedimento chamado pode alocar o armazenamento de heap e usar o identificador de contexto como um ponteiro para esse armazenamento.

Para fechar um identificador de contexto, o cliente passa o identificador de contexto como um **\[** argumento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** . O servidor deve retornar um identificador de contexto **nulo** quando ele não estiver mais mantendo o contexto em nome do chamador. Por exemplo, se o identificador de contexto representar um arquivo aberto e a chamada fechar o arquivo, o servidor deverá definir o identificador de contexto como **nulo** e retorná-lo ao cliente. Um valor **nulo** é inválido como um identificador de associação em chamadas subsequentes.

Um identificador de contexto só é válido para um servidor. Quando uma função tem dois parâmetros de identificador e o identificador de contexto não é **nulo**, os identificadores de associação devem se referir ao mesmo espaço de endereço.

Quando uma função tem um **\[** [](in.md) **\]** manipulador de contexto in ou **\[ in**, **out \]** , seu identificador de contexto pode ser usado como o identificador de associação. Nesse caso, a associação implícita não é usada e o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** ou o atributo de **\[** [**\_ identificador automático**](auto-handle.md) **\]** é ignorado.

As seguintes restrições se aplicam a identificadores de contexto:

-   Os identificadores de contexto não podem ser elementos de matriz, membros de estrutura ou membros de União. Eles só podem ser parâmetros.
-   Os identificadores de contexto não podem ter o **\[** atributo [**transmitir \_ como**](transmit-as.md) **\]** ou **\[** [**representar \_ como**](represent-as.md) **\]** .
-   Os parâmetros que são ponteiros para os **\[** [](out-idl.md) **\]** identificadores de contexto de saída devem ser **\[** [](ref.md) **\]** ponteiros de referência.
-   Um **\[** identificador [**de contexto in**](in.md) **\]** pode ser usado como o identificador de associação e não pode ser **nulo**.
-   Um identificador **\[ de contexto in**, [**out**](out-idl.md) pode ser **nulo** na entrada, mas somente se o procedimento tiver outro parâmetro de identificador explícito. Se não houver nenhum outro parâmetro de identificador de contexto não **nulo** explícito, o identificador **\[ de contexto in** e **out \]** não poderá ser **nulo**.
-   Um identificador de contexto não pode ser usado com retornos de chamada.

## <a name="examples"></a>Exemplos

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[Redefinição de contexto de cliente](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**processamento**](handle.md)
</dt> <dt>

[Associação e identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[Clientes multithread e identificadores de contexto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientContext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Rotina de execução de contexto de servidor](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 