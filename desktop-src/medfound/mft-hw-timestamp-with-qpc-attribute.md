---
description: Especifica se uma fonte de dispositivo de hardware usa a hora do sistema para carimbos de data/hora.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Atributo MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789610"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a>\_ \_ Carimbo de data/hora do HW \_ de MFT com \_ atributo de \_ atributo QPC

Especifica se uma fonte de dispositivo de hardware usa a hora do sistema para carimbos de data/hora.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, a origem do dispositivo usará a hora do sistema, conforme retornado pelo **QueryPerformanceCounter**, para carimbos de data/hora. Caso contrário, a origem do dispositivo usará o relógio do dispositivo. O valor padrão é **false**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




