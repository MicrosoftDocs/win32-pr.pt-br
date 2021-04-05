---
title: comutador/Pack
description: O comutador/Pack é o mesmo que a opção/ZP.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL do comutador/Pack
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006664"
---
# <a name="pack-switch"></a>comutador/Pack

O comutador **/Pack** é o mesmo que a opção [**/ZP**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nível de embalagem \_* 
</dt> <dd>

Especifica o nível de empacotamento das estruturas no sistema de destino. O valor de nível de embalagem pode ser definido como 1, 2, 4 ou 8.

</dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/Pack** designa o nível de empacotamento das estruturas no sistema de destino. O valor de nível de embalagem corresponde ao valor de opção [**/ZP**](-zp.md) usado pelo compilador Microsoft C/C++ versão 7,0. Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.

Especifique o mesmo nível de embalagem ao invocar o compilador MIDL e o compilador C. O nível de empacotamento padrão usado quando nem a opção [**/ZP**](-zp.md) nem **/Pack** é especificada é 8, em todos os ambientes de compilação.

Para obter uma discussão sobre os perigos potenciais no uso de níveis de embalagem não padrão, consulte o tópico da ajuda do [**/ZP**](-zp.md) .

## <a name="examples"></a>Exemplos

**MIDL/Pack 2 filename. idl**

**MIDL/Pack 8 bar. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




