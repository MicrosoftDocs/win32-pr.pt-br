---
description: Essa função força o programa de chamada se ele for invocado dentro de um texto explicativo do carregador. Caso contrário, ele não terá nenhum efeito.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Função LdrFastFailInLoaderCallout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754078"
---
# <a name="ldrfastfailinloadercallout-function"></a>Função LdrFastFailInLoaderCallout

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Essa função força o programa de chamada se ele for invocado dentro de um texto explicativo do carregador. Caso contrário, ele não terá nenhum efeito.

## <a name="syntax"></a>Sintaxe


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa rotina não captura todos os casos de deadlock em potencial; é possível que um thread dentro de um carregador de texto explicativo obtenha um bloqueio enquanto algum thread fora de um carregador de texto contém o mesmo bloqueio e faz uma chamada para o carregador. Em outras palavras, pode haver uma inversão de ordem de bloqueio entre o bloqueio de carregador e um bloqueio de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>NTDll. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




