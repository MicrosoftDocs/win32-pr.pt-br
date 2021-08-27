---
description: Observe que essa API foi preterida. Novos aplicativos não devem usá-lo. O tipo de dados MSPID identifica a finalidade de um fluxo de mídia.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d274fc4131c0aa4494d610cbe1145ad79b848b5f6280d4ad6a10b298a8b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075746"
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

 

 




