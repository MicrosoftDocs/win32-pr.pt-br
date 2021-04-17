---
description: Contém um ponteiro para a interface de retorno de chamada para o mecanismo de mídia.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: Atributo MF_MEDIA_ENGINE_CALLBACK (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782387"
---
# <a name="mf_media_engine_callback-attribute"></a>\_Atributo de \_ retorno de chamada do mecanismo de mídia MF \_

Contém um ponteiro para a interface de retorno de chamada para o mecanismo de mídia.

## <a name="data-type"></a>Tipo de dados

**IMFMediaEngineNotify \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , implementado pelo aplicativo.

Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia. O atributo é obrigatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




