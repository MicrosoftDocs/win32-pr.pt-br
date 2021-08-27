---
description: Especifica o tipo de processo identificado na estrutura D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE enumeração (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 522fee8421ec61b58bd67065c31b968252c2c7d563e94f7eda7a9f5105d20382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061976"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>Enumeração D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE

Especifica o tipo de processo identificado na estrutura [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT.**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ UNKNOWN**
</dt> <dd>

Tipo de processo desconhecido.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**
</dt> <dd>

Gerenciador de Janelas da Área de Trabalho (DWM).

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE \_ HANDLE**
</dt> <dd>

Lidar com um processo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types.h (inclua D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de vídeo do Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




