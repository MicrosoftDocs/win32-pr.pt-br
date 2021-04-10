---
description: Controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171802"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

O comando **pragma instanceflags** pré-processador controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.

O seguinte descreve a sintaxe:


```mof
#pragma instanceflags ([Flag])
```



O *\[ sinalizador \]* deve ser um dos argumentos a seguir.



| Sinalizador       | Descrição                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| somente | Impede que o compilador altere quaisquer instâncias existentes no arquivo MOF.                                |
| updateonly | Impede que o compilador crie novas instâncias se uma instância especificada no arquivo MOF não existir. |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar esse comando.


```mof
#pragma instanceflags("createonly")
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

 

 




