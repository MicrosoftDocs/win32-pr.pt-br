---
description: Exclui uma classe existente e suas instâncias do repositório.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma DeleteClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3cb62c9d90d5ac6346e25eaa3c254e0c6dd595805ec6901376ce9dccdf648289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996286"
---
# <a name="pragma-deleteclass"></a>pragma DeleteClass

O comando **pragma DeleteClass** pré-processador exclui uma classe existente e suas instâncias do repositório.

O seguinte descreve a sintaxe:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* é o nome da classe que o compilador do MOF exclui do namespace atual.

O *\[ sinalizador \]* deve ser um dos argumentos a seguir.



| Sinalizador   | Descrição                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| falha   | Faz com que o compilador MOF saia com uma mensagem de erro se a classe ainda não existir no repositório. |
| nofail | Faz com que o compilador MOF continue mesmo que a classe ainda não exista.                                |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar esse comando.


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 




