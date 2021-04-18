---
description: O tipo de dados HCRYPTKEY é usado para representar identificadores para chaves de criptografia.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770340"
---
# <a name="hcryptkey"></a>HCRYPTKEY

O tipo de dados **HCRYPTKEY** é usado para representar identificadores para [*chaves de criptografia*](../secgloss/c-gly.md). Esses identificadores são usados para indicar ao módulo CSP qual chave está sendo usada em uma operação específica. O módulo CSP não habilita o acesso direto aos valores de chave. Em vez disso, o usuário executa funções usando o valor de chave por meio do identificador de chave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
