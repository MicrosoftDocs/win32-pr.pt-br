---
title: /align switch
description: A opção /align é funcionalmente igual à opção MIDL /Zp e é reconhecida pelo compilador MIDL exclusivamente para compatibilidade com corretamente com MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align switch MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067646"
---
# <a name="align-switch"></a>/align switch

A **opção /align** é funcionalmente igual à opção MIDL [**/Zp**](-zp.md) e é reconhecida pelo compilador MIDL exclusivamente para compatibilidade com corretamente com MkTypLib.

> [!Note]  
> A Mktyplib.exe de dados está obsoleta. Em vez disso, use o compilador MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*Alinhamento* 
</dt> <dd>

Especifica o alinhamento para tipos na biblioteca. O *valor* de alinhamento pode ser 1, 2, 4 ou 8. O valor 1 indica alinhamento natural; *n* indica o alinhamento no byte *n*. Quando você não especifica a opção **/align,** o padrão é 8.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você estiver gerando um novo makefile, use a [**opção /Zp.**](-zp.md)

O valor de alinhamento corresponde ao [**valor da opção /Zp**](-zp.md) usado pelo compilador do Microsoft C/C++. Especifique o mesmo alinhamento ao invocar o compilador C quando invocar o compilador MIDL.

Para obter mais informações, consulte a documentação de programação do Microsoft C/C++. Para uma discussão sobre os possíveis riscos no uso de níveis de empacotamento não padrão, consulte o [**tópico ajuda /Zp.**](-zp.md)

## <a name="examples"></a>Exemplos

**midl /align:4 filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/zp**](-zp.md)
</dt> </dl>

 

 




