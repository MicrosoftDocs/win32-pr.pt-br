---
description: Especifica o campo predominância para um quadro de vídeo entrelaçado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Atributo MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296622"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>\_Atributo MFSampleExtension BottomFieldFirst

Especifica o campo predominância para um quadro de vídeo entrelaçado. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Se o quadro de vídeo estiver entrelaçado e o exemplo contiver dois campos intercalados, esse atributo indicará qual campo será exibido primeiro. Se **for true**, o campo inferior será o primeiro a ser atingido. Se for **false**, o campo superior será primeiro.

Se o quadro estiver entrelaçado e o exemplo contiver um único campo, esse atributo indicará qual campo contém o exemplo. Se **for true**, o exemplo conterá o campo inferior. Se **for false**, o exemplo conterá o campo superior.

Se o quadro for progressivo, esse atributo descreverá como os campos devem ser ordenados quando a saída for entrelaçada. Se **for true**, o campo inferior deverá ser de saída primeiro. Se **for false**, o campo superior deverá ser de saída primeiro.

Se esse atributo não estiver definido, o tipo de mídia descreverá o campo predominância.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> <dt>

[Entrelaçamento de vídeo](video-interlacing.md)
</dt> </dl>

 

 




