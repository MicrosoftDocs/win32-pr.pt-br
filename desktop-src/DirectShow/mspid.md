---
description: Observe que essa API foi preterida. Novos aplicativos não devem usá-lo. O tipo de dados MSPID identifica a finalidade de um fluxo de mídia.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758836"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Essa API está preterida. Novos aplicativos não devem usá-lo.

 

O tipo de dados **MSPID** identifica a finalidade de um fluxo de mídia.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Comentários

**MSPID** é simplesmente um TYPEDEF para GUID. Os MSPIDs a seguir são definidos.



| Valor               | Descrição           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Fluxo de vídeo primário. |
| MSPID \_ PrimaryAudio | Fluxo de áudio primário. |



 

O tipo **REFMSPID** define uma referência a um **MSPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mmstream. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados de streaming de multimídia](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




