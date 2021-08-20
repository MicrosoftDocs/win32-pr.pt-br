---
title: atributo vararg
description: O atributo \ vararg \ especifica que a função usa um número variável de parâmetros. Para fazer isso, o último parâmetro deve ser uma matriz segura de tipo VARIANT que contém todos os parâmetros restantes.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- atributo vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848393f6bad82d6793e34ba6f4da803c7dd64803c1c40e4ea05487ea141ec48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641004"
---
# <a name="vararg-attribute"></a>atributo vararg

O atributo **\[ vararg \]** especifica que a função usa um número variável de parâmetros. Para fazer isso, o último parâmetro deve ser uma matriz segura de tipo **Variant** que contém todos os parâmetros restantes.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opcional-atributos* 
</dt> <dd>

Especifica zero ou mais atributos a serem aplicados à função. Separe vários atributos com vírgulas.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados retornados pelo procedimento remoto após a conclusão.

</dd> <dt>

*Nome da função* 
</dt> <dd>

O nome do procedimento remoto.

</dd> <dt>

*Optional-parâmetros-atributos* 
</dt> <dd>

Especifica zero ou mais atributos a serem aplicados ao parâmetro de função imediatamente após a listagem de atributos.

</dd> <dt>

*parâmetro-lista* 
</dt> <dd>

Especifica todos os parâmetros, salve o parâmetro final, variável,.

</dd> <dt>

*Last-param-Name* 
</dt> <dd>

O nome do parâmetro variável.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você não pode aplicar os **\[** [](optional.md) **\]** atributos Optional ou **\[** [**DefaultValue**](defaultvalue.md) **\]** a quaisquer parâmetros em uma função que tenha o atributo **\[ vararg \]** .

## <a name="examples"></a>Exemplos

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ValorPadrão**](defaultvalue.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**adicional**](optional.md)
</dt> </dl>

 

 