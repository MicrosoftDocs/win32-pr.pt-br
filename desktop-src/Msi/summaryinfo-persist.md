---
description: O método Persist do objeto SummaryInfo formata e grava as propriedades armazenadas anteriormente no fluxo SummaryInformation padrão.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Método SummaryInfo. Persist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039596"
---
# <a name="summaryinfopersist-method"></a>Método SummaryInfo. Persist

O método **Persist** do objeto [**SummaryInfo**](summaryinfo-object.md) formata e grava as propriedades armazenadas anteriormente no fluxo SummaryInformation padrão. Ele gera um erro se o fluxo não puder ser gravado com êxito. Esse método só pode ser chamado uma vez depois que todos os valores de propriedade tiverem sido definidos. As propriedades ainda podem ser lidas depois que o fluxo é gravado.

## <a name="syntax"></a>Sintaxe


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




