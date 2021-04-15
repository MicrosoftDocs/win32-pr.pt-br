---
title: comutador/align
description: O comutador/align é funcionalmente o mesmo que a opção MIDL/ZP e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- MIDL do comutador/align
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498893"
---
# <a name="align-switch"></a>comutador/align

O comutador **/align** é funcionalmente o mesmo que a opção MIDL [**/ZP**](-zp.md) e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib.

> [!Note]  
> A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*sintonia* 
</dt> <dd>

Especifica o alinhamento dos tipos na biblioteca. O valor de *alinhamento* pode ser 1, 2, 4 ou 8. O valor 1 indica o alinhamento natural; *n* indica alinhamento no byte *n*. Quando você não especificar a opção **/align** , o padrão será 8.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você estiver gerando um novo makefile, use a opção [**/ZP**](-zp.md) .

O valor de alinhamento corresponde ao valor da opção [**/ZP**](-zp.md) usado pelo compilador C/C++ da Microsoft. Certifique-se de especificar o mesmo alinhamento ao invocar o compilador C como quando você invoca o compilador MIDL.

Para obter mais informações, consulte a documentação de programação do Microsoft C/C++. Para obter uma discussão sobre os perigos potenciais no uso de níveis de embalagem não padrão, consulte o tópico da ajuda do [**/ZP**](-zp.md) .

## <a name="examples"></a>Exemplos

**MIDL/align: 4 nome de arquivo. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




