---
title: atributo público
description: O atributo \ public\ inclui um alias declarado com a palavra-chave typedef na biblioteca de tipos.
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
ms.openlocfilehash: 9f8e4944404bccc734594f3847c0ff9de17e54d0b5bcc444a56abe9b8f1e0eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328716"
---
# <a name="public-attribute"></a>atributo público

O **\[ atributo \]** público inclui um alias declarado com a [**palavra-chave typedef**](typedef.md) na biblioteca de tipos.

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

Outro nome pelo qual *o tipo de dados* será conhecido no software.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, um alias que é declarado com [**typedef**](typedef.md) e não tem outros atributos é tratado como um **\# define** e não está incluído na biblioteca de tipos. Usar o **\[ atributo \]** público garante que o alias se torne parte da biblioteca de tipos.

> [!Note]  
> O compilador MIDL requer que você aplique explicitamente o **\[ atributo \]** público a cada typedef que você deseja público.

 

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

[**Interface**](interface.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 