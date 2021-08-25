---
description: Especifica informações de quadro de referência de longo prazo (EPD) e retornadas no exemplo de saída.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Atributo MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642c246adf0e5e1c10249085201fba3dc430b6547516b79fe4929e9de4b998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848116"
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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




