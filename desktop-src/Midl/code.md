---
title: atributo de código
description: O atributo \ Code \ ACF faz com que o código stub do cliente seja gerado para funções remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- código de MIDL do atributo code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293356"
---
# <a name="code-attribute"></a>atributo de código

O atributo de ACF de **\[ código \]** faz com que o código stub do cliente seja gerado para funções remotas.

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

*ACF-interface-atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo. Os atributos válidos incluem o [**\[ \_ identificador \] automático**](auto-handle.md) ou o [**\[ \_ \] identificador implícito**](implicit-handle.md) e o **\[ código \]**, [**\[ Nocode \]**](nocode.md)ou [**\[ Optimize \]**](optimize.md). Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*nome do arquivo-lista* 
</dt> <dd>

Especifica uma lista de um ou mais nomes de arquivo de cabeçalho C, separados por vírgulas. Você deve fornecer o nome completo do arquivo, incluindo a extensão.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo especificado. Atributos de tipo válidos incluem [**\[ \] alocar**](allocate.md) e [**\[ representar \_ como \]**](represent-as.md).

</dd> <dt>

*TypeName* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL. Os atributos de tipo no ACF podem ser aplicados somente aos tipos definidos anteriormente no arquivo IDL.

</dd> <dt>

*ACF-função-atributos* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função como um todo, como o [**\[ \_ status \] de comunicação**](comm-status.md). Os atributos de função são colocados entre colchetes. Separe vários atributos de função com vírgulas.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parâmetros-atributos* 
</dt> <dd>

Especifica atributos de ACF que se aplicam a um parâmetro. Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro. Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro de ACF são colocados entre colchetes.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica um parâmetro da função, conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência e com o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ Code \]** pode aparecer no cabeçalho ACF ou ser aplicado a uma função individual.

Quando o atributo de **\[ código \]** é exibido no cabeçalho ACF, o código stub do cliente é gerado para todas as funções remotas que não têm o atributo função [**\[ Nocode \]**](nocode.md) . Você pode substituir o atributo de **\[ código \]** no cabeçalho de uma função individual especificando o atributo **\[ Nocode \]** como um atributo de função.

Quando o atributo de **\[ código \]** é exibido na lista de atributos da função remota, o código stub do cliente é gerado para a função. O código stub do cliente não é gerado quando:

-   O cabeçalho ACF inclui o atributo [**\[ Nocode \]**](nocode.md) .
-   O atributo [**\[ Nocode \]**](nocode.md) é aplicado à função.
-   O atributo [**\[ local \]**](local.md) se aplica à função no arquivo de interface.

O **\[ código \]** ou o [**\[ Nocode \]**](nocode.md) podem aparecer na lista de atributos da interface ou da função, mas o que você escolher pode aparecer apenas uma vez na lista.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**status de comunicação \_**](comm-status.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> <dt>

[**formato**](optimize.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> </dl>

 

 




