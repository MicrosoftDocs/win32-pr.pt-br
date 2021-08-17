---
title: atributo de código
description: O atributo \ code\ ACF faz com que o código stub do cliente seja gerado para funções remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- atributo de código MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d94f4f764fb25e5e2a5a43d1cdbe76f5288901846c2291daa4497947a486f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991810"
---
# <a name="code-attribute"></a>atributo de código

O **\[ atributo \]** ACF de código faz com que o código stub do cliente seja gerado para funções remotas.

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Atributos de interface ACF* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo. Os atributos válidos [**\[ incluem o handle \_ \] automático**](auto-handle.md) [**\[ ou o alça \_ \] implícito**](implicit-handle.md) e o **\[ código \]**, [**\[ nocode \]**](nocode.md)ou [**\[ optimize \]**](optimize.md). Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*filename-list* 
</dt> <dd>

Especifica uma lista de um ou mais nomes de arquivo de c-header, separados por vírgulas. Você deve fornecer o nome completo do arquivo, incluindo a extensão.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo especificado. Atributos de tipo [**\[ válidos incluem \] alocar**](allocate.md) e representar [**\[ \_ como \]**](represent-as.md).

</dd> <dt>

*Typename* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL. Atributos de tipo no ACF podem ser aplicados somente a tipos definidos anteriormente no arquivo IDL.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função como um todo, como o [**\[ status de \_ vírgula \]**](comm-status.md). Os atributos de função são incluídos entre colchetes. Separe vários atributos de função com vírgulas.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica atributos ACF que se aplicam a um parâmetro. Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro . Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro ACF são incluídos entre colchetes.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica um parâmetro da função conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência e com o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \]** de código pode aparecer no header do ACF ou ser aplicado a uma função individual.

Quando o **\[ atributo \]** de código aparece no header ACF, o código stub do cliente é gerado para todas as funções remotas que não têm o [**\[ atributo de função nocode. \]**](nocode.md) Você pode substituir o **\[ atributo \]** de código no header de uma função individual especificando o **\[ atributo nocode \]** como um atributo de função.

Quando o **\[ atributo \]** de código aparece na lista de atributos da função remota, o código stub do cliente é gerado para a função. O código stub do cliente não é gerado quando:

-   O header do ACF inclui o [**\[ atributo nocode. \]**](nocode.md)
-   O [**\[ atributo \] nocode**](nocode.md) é aplicado à função .
-   O [**\[ atributo local \]**](local.md) se aplica à função no arquivo de interface.

O **\[ código \]** ou [**\[ nocode \]**](nocode.md) pode aparecer na interface ou na lista de atributos de função, mas o que você escolher pode aparecer apenas uma vez na lista.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Alocar**](allocate.md)
</dt> <dt>

[**auto \_ handle**](auto-handle.md)
</dt> <dt>

[**status do \_ comm**](comm-status.md)
</dt> <dt>

[**alça \_ implícita**](implicit-handle.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Otimizar**](optimize.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> </dl>

 

 




