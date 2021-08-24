---
description: Contém um ponteiro para a interface de retorno de chamada para o Mecanismo de Mídia.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: MF_MEDIA_ENGINE_CALLBACK atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ba6149c8d0b615ad13277588bbee5ee7397d9adaa089195671b3336b2b406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723039"
---
# <a name="mf_media_engine_callback-attribute"></a>Atributo \_ CALLBACK do MECANISMO \_ DE MÍDIA \_ MF

Contém um ponteiro para a interface de retorno de chamada para o Mecanismo de Mídia.

## <a name="data-type"></a>Tipo de dados

**IMFMediaEngineNotify \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFMediaEngineNotify,**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) implementada pelo aplicativo.

Esse atributo é usado com o [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o Mecanismo de Mídia. O atributo é obrigatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




