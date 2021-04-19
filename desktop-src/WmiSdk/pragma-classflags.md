---
description: Controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796071"
---
# <a name="pragma-classflags"></a>pragma classflags

O comando **pragma classflags** pré-processador controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.

O seguinte descreve a sintaxe para este comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



O *\[ sinalizador \]* deve ser um ou mais dos argumentos a seguir. Você pode combinar qualquer sinalizador que não se contradizer.



| Sinalizador        | Descrição                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| somente  | Instrui o compilador a não fazer nenhuma alteração nas classes existentes e encerrar uma compilação se uma classe especificada no arquivo MOF já existir no WMI.                                                                                                                                                                                                        |
| forceupdate | Força atualizações de classes quando existem classes filhas conflitantes. Por exemplo, se você definir um qualificador de classe em uma classe filho e a classe base tentar adicionar o mesmo qualificador, o uso desse sinalizador fará com que o compilador resolva esse conflito excluindo o qualificador conflitante na classe filho. Se a classe filho tiver instâncias, a atualização falhará. |
| safeupdate  | Permite que o compilador atualize classes mesmo se houver classes filhas, se a alteração não causar conflitos com classes filhas. Por exemplo, esse sinalizador permite que você adicione uma nova propriedade a uma classe base sem também precisar adicionar a propriedade a nenhuma classe filho pré-existente. Se as classes filhas tiverem instâncias, a atualização falhará.                           |
| updateonly  | Instrui o compilador a não criar novas classes e faz com que o compilador encerre a compilação se uma classe especificada no arquivo MOF não existir.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar esse comando com os sinalizadores UpdateOnly e forceupdate.


```mof
#pragma classflags ("updateonly", "forceupdate")
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

 

 




