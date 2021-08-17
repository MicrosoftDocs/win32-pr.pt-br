---
title: atributo Nocode
description: O atributo \ Nocode \ é usado em cabeçalhos ACF ou com funções individuais para evitar a geração de código stub de cliente.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- MIDL de atributo Nocode
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ec4612bc1bd5db1a8cdcbecdced51911591cdf5c482c83381f86deafd66a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066956"
---
# <a name="nocode-attribute"></a>atributo Nocode

O atributo **\[ Nocode \]** é usado em cabeçalhos ACF ou com funções individuais para evitar a geração de código stub de cliente.

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ACF-interface-atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos que se aplicam à interface como um todo. Os atributos válidos incluem o **\[** [**\_ identificador automático**](auto-handle.md) **\]** ou o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** e o **\[** [**código**](code.md) **\]** ou **\[ \] Nocode**. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface. No modo de compatibilidade com DCE, o nome da interface deve corresponder ao nome da interface especificada no arquivo IDL. Quando você usa o switch do compilador MIDL [**/ACF**](-acf.md), o nome da interface no ACF e o nome da interface no arquivo IDL podem ser diferentes.

</dd> <dt>

*nome do arquivo-lista* 
</dt> <dd>

Especifica uma lista de um ou mais nomes de arquivos de cabeçalho de linguagem C, separados por vírgulas. O nome completo do arquivo, incluindo a extensão, deve ser fornecido.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao tipo especificado. Os atributos de tipo válidos incluem **\[** [**ALLOCATE**](allocate.md) **\]** .

</dd> <dt>

*TypeName* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL. Os atributos de tipo no ACF só podem ser aplicados a tipos definidos anteriormente no arquivo IDL.

</dd> <dt>

*ACF-função-atributos* 
</dt> <dd>

Especifica os atributos que se aplicam à função como um todo, como o **\[** [**\_ status de comunicação**](comm-status.md) **\]** . Os atributos de função são colocados entre colchetes. Separe vários atributos de função com vírgulas.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parâmetros-atributos* 
</dt> <dd>

Especifica atributos de ACF que se aplicam a um parâmetro. Observe que zero ou mais atributos podem ser aplicados ao parâmetro. Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro de ACF são colocados entre colchetes.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica um parâmetro da função, conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência e usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ Nocode \]** pode aparecer no cabeçalho ACF ou pode ser aplicado a uma função individual.

Quando o atributo **\[ \] Nocode** aparece no cabeçalho ACF, o código stub do cliente não é gerado para nenhuma função remota, a menos que ele tenha o atributo de função de **\[** [**código**](code.md) **\]** . Você pode substituir o atributo **\[ Nocode \]** no cabeçalho de uma função individual especificando o atributo de **\[ código \]** como um atributo de função.

Quando o atributo **\[ Nocode \]** aparece na lista de atributos da função, nenhum código stub do cliente é gerado para a função.

O código stub do cliente não é gerado quando:

-   O cabeçalho ACF inclui o atributo **\[ Nocode \]** .
-   O atributo **\[ Nocode \]** é aplicado à função.
-   O **\[** [](local.md) **\]** atributo local se aplica à função no arquivo de interface.

O **\[** [**código**](code.md) **\]** ou o **\[ Nocode \]** podem aparecer na lista de atributos de uma função e o que você escolher pode aparecer exatamente uma vez.

O atributo **\[ Nocode \]** é ignorado quando stubs de servidor são gerados. Você não pode aplicá-lo ao gerar stubs de servidor no modo de compatibilidade de DCE.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**auto-completar**](code.md)
</dt> <dt>

[**status de comunicação \_**](comm-status.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> </dl>

 

 




