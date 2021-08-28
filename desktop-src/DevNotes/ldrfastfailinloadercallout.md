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
ms.openlocfilehash: f944de64f26d814af799d1f8d2419c2dd9ade04970774e2581f446c0bd32c0fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001326"
---
# <a name="ldrfastfailinloadercallout-function"></a>Função LdrFastFailInLoaderCallout

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Essa função força o programa de chamada se ele for invocado dentro de um texto explicativo do carregador. Caso contrário, ele não terá nenhum efeito.

## <a name="syntax"></a>Sintaxe


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa rotina não captura todos os casos de deadlock em potencial; é possível que um thread dentro de um carregador de texto explicativo obtenha um bloqueio enquanto algum thread fora de um carregador de texto contém o mesmo bloqueio e faz uma chamada para o carregador. Em outras palavras, pode haver uma inversão de ordem de bloqueio entre o bloqueio de carregador e um bloqueio de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>NTDll. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




