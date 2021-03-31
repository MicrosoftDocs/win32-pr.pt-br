---
description: Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Propriedade MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661833"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>\_Propriedade MFPKEY WMAVOICE \_ ENC \_ EDL

Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo de Dados

VT \_ BSTR

## <a name="default-value"></a>Valor padrão

Sem valor padrão. Se essa propriedade não for definida, o codec usará o valor da propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar como codificar o conteúdo.

## <a name="remarks"></a>Comentários

Você pode usar essa propriedade se o modo automático do codec não estiver fornecendo resultados satisfatórios.

Esse valor é uma cadeia de caracteres delimitada por vírgula que contém pelo menos quatro inteiros. O primeiro inteiro é o número de versão; Sempre use 1 para esse valor. O segundo inteiro é o número de seções que precisam ser codificadas como música. Seguindo o segundo inteiro há um número de pares de valores representando intervalos em milissegundos, um par para cada seção de conteúdo que precisa ser codificado como música.

Por exemplo, "1, 2100200500600" informa o codificador para usar a versão 1 com 2 seções de música. A primeira seção de música começa às 100 ms e termina em 200 ms. A segunda seção de música começa às 500 MS e termina em 600 MS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




