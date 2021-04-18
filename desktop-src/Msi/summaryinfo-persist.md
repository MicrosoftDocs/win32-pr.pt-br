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
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810314"
---
# <a name="summaryinfopersist-method"></a>Método SummaryInfo. Persist

O método **Persist** do objeto [**SummaryInfo**](summaryinfo-object.md) formata e grava as propriedades armazenadas anteriormente no fluxo SummaryInformation padrão. Ele gera um erro se o fluxo não puder ser gravado com êxito. Esse método só pode ser chamado uma vez depois que todos os valores de propriedade tiverem sido definidos. As propriedades ainda podem ser lidas depois que o fluxo é gravado.

## <a name="syntax"></a>Sintaxe


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




