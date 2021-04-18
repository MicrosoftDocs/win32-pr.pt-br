---
description: O atributo que é passado no IMFMediaEngineNeedKeyNotify para o mecanismo de mídia na criação.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763916"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>\_Atributo de \_ retorno de \_ chamada NEEDKEY do mecanismo de mídia MF \_

O atributo que é passado no [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) para o mecanismo de mídia na criação.

## <a name="data-type"></a>Tipo de dados

**IMFMediaEngineNeedKeyNotify \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implementado pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




