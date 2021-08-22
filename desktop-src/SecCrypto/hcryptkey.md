---
description: O tipo de dados HCRYPTKEY é usado para representar identificadores para chaves de criptografia.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006434"
---
# <a name="hcryptkey"></a>HCRYPTKEY

O tipo de dados **HCRYPTKEY** é usado para representar identificadores para [*chaves de criptografia*](../secgloss/c-gly.md). Esses identificadores são usados para indicar ao módulo CSP qual chave está sendo usada em uma operação específica. O módulo CSP não habilita o acesso direto aos valores de chave. Em vez disso, o usuário executa funções usando o valor de chave por meio do identificador de chave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
