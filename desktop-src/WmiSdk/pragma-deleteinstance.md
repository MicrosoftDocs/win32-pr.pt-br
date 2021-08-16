---
description: Exclui uma instância existente de uma classe do repositório.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316837"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

O **comando pragma deleteinstance** exclui uma instância existente de uma classe do repositório.

O seguinte descreve a sintaxe para este comando:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* é um identificador exclusivo da instância que o compilador MOF exclui do namespace atual.

*\[ O \]* sinalizador deve ser um dos argumentos a seguir.



| Sinalizador   | Descrição                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| falha   | Faz com que o compilador MOF saia com uma mensagem de erro se a classe ainda não existir no repositório. |
| nofail | Faz com que o compilador MOF continue mesmo que a classe ainda não exista.                                |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar esse comando.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




