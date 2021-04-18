---
title: atributo público
description: O atributo \ Public \ inclui um alias declarado com a palavra-chave typedef na biblioteca de tipos.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- atributo público MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752058"
---
# <a name="public-attribute"></a>atributo público

O atributo **\[ \] Public** inclui um alias declarado com a palavra-chave [**typedef**](typedef.md) na biblioteca de tipos.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de dados* 
</dt> <dd>

O tipo de dados para o qual o identificador será um alias.

</dd> <dt>

*identifier* 
</dt> <dd>

Outro nome pelo qual o *tipo de dados* será conhecido no software.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, um alias declarado com [**typedef**](typedef.md) e nenhum outro atributo é tratado como uma **\# definição** e não é incluído na biblioteca de tipos. O uso do atributo **\[ Public \]** garante que o alias se torne parte da biblioteca de tipos.

> [!Note]  
> O compilador MIDL requer que você aplique explicitamente o atributo **\[ Public \]** a cada TypeDef que você deseja público.

 

## <a name="examples"></a>Exemplos

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 