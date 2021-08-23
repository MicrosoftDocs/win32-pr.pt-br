---
description: Especifica se o decodificador deve executar Lt-Rt dobra para baixo.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76d086fd0f57262d249784fcabc5a98e8a18668cf0697618f3fbbe5528a2cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713806"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>Propriedade MFPKEY \_ WALTC \_ LTRTOUTPUT

Especifica se o decodificador deve executar Lt-Rt dobra para baixo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**BOOL da VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentários

Se essa propriedade tiver um valor de VARIANT FALSE e a saída for estéreo, o \_ decodificador de áudio usará uma dobra de canal simples para baixo. Se essa propriedade tiver um valor de VARIANT TRUE, o Lt-Rt decodificador de áudio executará uma dobra (matrizizada) para baixo para estéreo e, em seguida, qualquer decodificador Surround Dolby poderá ser usado para decodificar o surround matriz. \_ Por exemplo, o decodificador de áudio pode executar Lt-Rt dobra para baixo no conteúdo 5.1 ou 7.1.

Essa propriedade só tem suporte quando o decodificador está atuando como um objeto de mídia directX (DMO). Nenhuma dobra para baixo de qualquer tipo é suportada quando o decodificador está atuando como uma transformação Media Foundation (MFT).

No Windows Vista, se você obter uma interface **IPropertyStore** em um decodificador de áudio, o decodificador atuará como um MFT. Consequentemente, essa propriedade não pode ser usada no Windows Vista. Para obter informações sobre quando um decodificador atua como um DMO ou um MFT, consulte as páginas de referência de codec individuais em [Objetos Codec](codecobjects.md).

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

 

 
