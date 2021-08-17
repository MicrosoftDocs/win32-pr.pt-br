---
title: atributo retval
description: O atributo \ retval \ designa o parâmetro que recebe o valor de retorno do membro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- atributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72655883b24c83890cf2f5604cb8f7335c6943b32e5e69611dba415689b03e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146299"
---
# <a name="retval-attribute"></a>atributo retval

O atributo **\[ retval \]** designa o parâmetro que recebe o valor de retorno do membro.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo de dados do valor de retorno do procedimento remoto.

</dd> <dt>

*Nome da função* 
</dt> <dd>

O nome usado para invocar o procedimento remoto.

</dd> <dt>

*opcional-atributos* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de dados* 
</dt> <dd>

O tipo dos dados passados pelo parâmetro.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

O nome do identificador do parâmetro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar o atributo **\[ retval \]** em parâmetros de membros de interface que descrevem métodos ou obter propriedades. (O atributo é necessário no último parâmetro de um método que tem o **\[** [**propget**](propget.md) **\]** atributo.) O parâmetro deve ter o **\[** atributo [**out**](out-idl.md) **\]** e deve ser um tipo de ponteiro.

Você não pode aplicar o **\[** atributo [**opcional**](optional.md) **\]** a um parâmetro **\[ \] retval** .

O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):

1.  Parâmetros obrigatórios (parâmetros que não têm os **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** ou **\[** [**optional**](optional.md) **\]** ).
2.  Parâmetros opcionais com ou sem o **\[** [](defaultvalue.md) **\]** atributo DefaultValue.
3.  Parâmetros com o **\[** atributo [**opcional**](optional.md) **\]** e sem o **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .
4.  **\[** parâmetro [**LCID**](lcid.md) **\]** , se houver.
5.  parâmetro **\[ retval \]** .

Os parâmetros com o atributo **\[ retval \]** não são exibidos em navegadores orientados ao usuário.

### <a name="flags"></a>Flags

IDLFLAG \_ FRETVAL

## <a name="examples"></a>Exemplos

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ValorPadrão**](defaultvalue.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**adicional**](optional.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 