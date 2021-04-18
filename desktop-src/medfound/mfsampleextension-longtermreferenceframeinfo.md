---
description: Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Atributo MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105767800"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>\_Atributo MFSampleExtension LongTermReferenceFrameInfo

Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

Os codificadores devem retornar esse atributo no exemplo de saída quando o aplicativo controla quadros EPD, que é especificado por [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

MFSampleExtension \_ LongTermReferenceFrameInfo retorna até dois campos.

O primeiro campo, bits \[ 0.. 15 \] , é *LongTermFrameIdx* associado ao quadro de saída se estiver marcado como um quadro EPD. O primeiro valor é 0xffff, se esse quadro de saída for um quadro de referência de curto prazo ou um quadro que não seja de referência.

O segundo campo, bits \[ 16.. 31 \] , é um bitmap que consiste em *MaxNumLTRFrames* muitos bits que indicam quais quadros EPD foram usados para codificar esse quadro de saída, começando do bit 16. O restante dos bits deve ser definido como 0. O segundo valor será 0 se esse quadro de saída não for codificado usando quadros EPD. *MaxNumLTRFrames* é o número máximo de quadros EPD definido por meio de [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




