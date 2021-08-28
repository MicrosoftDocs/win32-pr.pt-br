---
description: Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc9f68c7122897c9f5032e9ac0e4fc93c596b5ce65f18d44fb6af6dff2dd2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713716"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>Propriedade EDL MFPKEY \_ WMAVOICE \_ ENC \_

Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo de Dados

VT \_ BSTR

## <a name="default-value"></a>Valor padrão

Sem valor padrão. Se essa propriedade não estiver definida, o codec usará o valor da propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar como codificar o conteúdo.

## <a name="remarks"></a>Comentários

Você poderá usar essa propriedade se o modo automático do codec não estiver dando resultados satisfatórios.

Esse valor é uma cadeia de caracteres delimitada por vírgula que contém pelo menos quatro inteiros. O primeiro inteiro é o número de versão; sempre use 1 para esse valor. O segundo inteiro é o número de seções que precisam ser codificadas como música. Após o segundo inteiro estão vários pares de valores que representam intervalos em milissegundos, um par para cada seção de conteúdo que precisa ser codificado como música.

Por exemplo, "1,2.100.200.500.600" informa o codificador para usar a versão 1 com duas seções de música. A primeira seção de música começa em 100 ms e termina em 200 ms. A segunda seção de música começa em 500 ms e termina em 600 ms.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




