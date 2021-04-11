---
description: Especifica dados de controle de fatia.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Estrutura de DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010311"
---
# <a name="dxva_slice_hevc_short-structure"></a>\_Estrutura curta da fatia de DXVA \_ HEVC \_

Especifica dados de controle de fatia.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Membros

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

Especifica o local da unidade NAL.

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

O número de bytes no buffer de dados fragmentado que estão associados a essa estrutura de dados de controle de fatia.

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

Se a análise fragmentado fora do host for usada, esse valor indicará a fatia inadequada que está sendo desativada e conterá um dos seguintes valores:



| Requisito | Valor |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor | Descrição                                                                                                                                                                                                                                             |
| 0     | Todos os bits da fatia estão localizados no buffer de dados fragmentado correspondente.                                                                                                                                                                      |
| 1     | O buffer de dados fragmentado contém o início da fatia, mas não toda a fatia, porque o buffer está cheio.                                                                                                                                        |
| 2     | O buffer de dados fragmentado contém o fim da fatia. Ele não contém o início da fatia, pois o início da fatia estava localizado no buffer de dados fragmentado anterior.                                                                  |
| 3     | O buffer de dados fragmentado não contém o início da fatia porque o início da fatia estava localizado no buffer de dados fragmentado anterior e não contém o final da fatia, pois o buffer de dados fragmentado atual também está cheio. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

**DXVA \_ Fatia \_ HEVC \_ Short** contém dados de controle de fatia que são passados para o acelerador de hardware do decodificador de software do host.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




