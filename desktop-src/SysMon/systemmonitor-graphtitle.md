---
title: Propriedade SystemMonitor. GraphTitle
description: Recupera ou define o título do grafo.
ms.assetid: 10a91b38-6963-4ef6-8b4f-9ecd1341f471
keywords:
- Propriedade GraphTitle SysMon
- Propriedade GraphTitle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade GraphTitle
topic_type:
- apiref
api_name:
- SystemMonitor.GraphTitle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55918b67eb88b8c2c1aca99ce6e86f190ad1a395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499380"
---
# <a name="systemmonitorgraphtitle-property"></a>Propriedade SystemMonitor. GraphTitle

Recupera ou define o título do grafo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property GraphTitle As String
```



## <a name="property-value"></a>Valor da propriedade

Título do grafo. O comprimento máximo do título é de 128 caracteres. Se o título exceder 128 caracteres, o título será truncado.

**Windows XP e windows 2000:** Não há nenhum limite para o comprimento do título.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





