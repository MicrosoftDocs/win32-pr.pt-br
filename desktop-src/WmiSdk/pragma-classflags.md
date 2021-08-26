---
description: Controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: classflags pragma
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
ms.openlocfilehash: 6fd2b8ec75bd0521ce31af1ee7ce9dba2d9498890f9b5ddc768463f733322cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996316"
---
# <a name="pragma-classflags"></a>classflags pragma

O **comando pré-processador pragma classflags** controla a maneira como o WMI cria ou atualiza classes dependendo dos sinalizadores especificados.

O seguinte descreve a sintaxe para este comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



*\[ O \]* sinalizador deve ser um ou mais dos argumentos a seguir. Você pode combinar todos os sinalizadores que não contradimentam uns aos outros.



| Sinalizador        | Descrição                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Instrui o compilador a não fazer nenhuma alteração em classes existentes e encerra uma compilação se uma classe especificada no arquivo MOF já existir no WMI.                                                                                                                                                                                                        |
| forceupdate | Força atualizações de classes quando existem classes filho conflitantes. Por exemplo, se você definir um qualificador de classe em uma classe filho e a classe base tentar adicionar o mesmo qualificador, o uso desse sinalizador faz com que o compilador resolva esse conflito excluindo o qualificador conflitante na classe filho. Se a classe filho tiver instâncias, a atualização falhará. |
| safeupdate  | Permite que o compilador atualize classes mesmo se existirem classes filho, se a alteração não causar conflitos com classes filho. Por exemplo, esse sinalizador permite que você adicione uma nova propriedade a uma classe base sem também precisar adicionar a propriedade a qualquer classe filho pré-existente. Se as classes filho têm instâncias, a atualização falha.                           |
| updateonly  | Instrui o compilador a não criar nenhuma nova classe e faz com que o compilador encerre a compilação se uma classe especificada no arquivo MOF não existir.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar esse comando com os sinalizadores updateonly e forceupdate.


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

 

 




