---
title: atributo oleautomation
description: Atributo MIDL oleautomation e compatibilidade com automação.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- oleautomation do atributo MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007529"
---
# <a name="oleautomation-attribute"></a>atributo oleautomation

O atributo **oleautomation** indica que uma interface é compatível com a automação.

``` syntax
[ 
    oleautomation, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
    ...
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cadeia de caracteres-UUID* 
</dt> <dd>

Especifica uma cadeia de caracteres UUID gerada pelo utilitário Uuidgen.

</dd> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

Especifica o nome de uma interface de automação da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface. Todas as interfaces de automação são derivadas de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os parâmetros e os tipos de retorno especificados para os membros de uma interface **\[ oleautomation \]** devem ser compatíveis com a automação, conforme listado na tabela a seguir.



| Tipo                                            | Descrição                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **booleano**                                     | Item de dados que pode ter o valor VARIANT \_ true ou Variant \_ false. O tamanho corresponde a VARIANT \_ bool.                                                                                                     |
| **unsigned char**                               | item de dados não assinado de 8 bits.                                                                                                                                                                                     |
| **double**                                      | número de ponto flutuante IEEE de 64 bits.                                                                                                                                                                            |
| **float**                                       | número de ponto flutuante IEEE de 32 bits.                                                                                                                                                                            |
| **int**                                         | Inteiro com sinal, cujo tamanho é dependente do sistema. Em plataformas de 32 bits, MIDL trata [**int**](int.md) como um inteiro com sinal de 32 bits.                                                                               |
| **longo**                                        | Inteiro com sinal de 32 bits.                                                                                                                                                                                        |
| **short**                                       | inteiro de 16 bits com sinal.                                                                                                                                                                                        |
| **BSTR**                                        | Cadeia de caracteres de comprimento prefixado, conforme descrito no tópico de automação [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | número de ponto flutuante fixo de 8 bytes.                                                                                                                                                                          |
| **DATE**                                        | 64 bits, número fracionário de ponto flutuante de dias desde 30 de dezembro de 1899.                                                                                                                                     |
| **SCODE**                                       | Para sistemas de 16 bits – tipo de erro interno que corresponde ao erro de VT \_ .                                                                                                                                         |
| **Enumeração de typedef** Â  *MyEnum*                      | Inteiro com sinal, cujo tamanho é dependente do sistema.                                                                                                                                                               |
| **Interface IDispatch \***                      | Ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ( \_ expedição VT).                                                                                                                |
| **Interface IUnknown \***                       | Ponteiro para uma interface que não deriva de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ desconhecido). (Qualquer interface OLE pode ser representada por sua interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .) |
| **dispinterface** @ *TypeName \**                | Ponteiro para uma interface derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Dispatch).                                                                                                    |
| **Coclass** @ *TypeName \**                      | Ponteiro para um nome de coclasse (VT \_ desconhecido).                                                                                                                                                                      |
| **\[ \] interface oleautomation** Â   *TypeName \** | Ponteiro para uma interface que deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SafeArray**(*TypeName*)                       | *TypeName* é qualquer um dos tipos acima. Matriz desses tipos.                                                                                                                                                   |
| **TypeName \***                                 | *TypeName* é qualquer um dos tipos acima. Ponteiro para um tipo.                                                                                                                                                      |
| **Decimal**                                     | inteiro binário sem sinal de 96 bits dimensionado por uma potência variável de 10. Um tipo de dados decimal que fornece um tamanho e uma escala para um número (como em coordenadas).                                                       |



 

Um parâmetro é compatível com a automação se seu tipo é um tipo compatível com automação, um ponteiro para um tipo compatível com automação ou uma SAFEARRAY de um tipo compatível com a automação.

Um tipo de retorno será compatível com a automação se seu tipo for HRESULT, SCODE ou [**void**](void.md). No entanto, MIDL requer que os métodos de interface retornem HRESULT ou SCODE. Retornar **void** gera um erro de compilador.

Um membro será compatível com a automação se seu tipo de retorno e todos os seus parâmetros forem compatíveis com a automação.

Uma interface é compatível com a automação se for derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ou [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), ela tem o atributo **\[ oleautomation \]** e todas as suas entradas de VTBL são compatíveis com a automação. Para plataformas de 32 bits, a Convenção de chamada para todos os métodos na interface deve ser STDCALL. Para sistemas de 16 bits, todos os métodos devem ter a Convenção de chamada CDECL.

Cada [**dispinterface**](dispinterface.md) é implicitamente compatível com automação. Portanto, você não deve usar o atributo **\[ \] oleautomation** no **dispinterface**.

O atributo **\[ \] oleautomation** não está disponível quando você compila usando a opção [**/OSF**](-osf.md) do compilador MIDL.

### <a name="flags"></a>Flags

TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Exemplos

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> </dl>

 

 