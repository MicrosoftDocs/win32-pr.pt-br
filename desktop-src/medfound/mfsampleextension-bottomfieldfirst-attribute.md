---
description: Especifica o campo predominância para um quadro de vídeo entrelaçado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Atributo MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113066"
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
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

 

 




