---
description: Especifica se o decodificador deve executar Lt-Rt dobra para baixo.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Propriedade MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091067"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>\_Propriedade MFPKEY WMADEC \_ LTRTOUTPUT

Especifica se o decodificador deve executar Lt-Rt dobra para baixo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Se essa propriedade tiver um valor de variante \_ false e a saída for estéreo, o decodificador de áudio usará a dobra de canal simples. Se essa propriedade tiver um valor de VARIANT \_ true, o decodificador de áudio executará Lt-Rt (em matriz) com dobra para estéreo e qualquer decodificador Dolby Surround poderá ser usado para decodificar o surround em matriz. Por exemplo, o decodificador de áudio poderia executar Lt-Rt dobrar no conteúdo 5,1 ou 7,1.

Essa propriedade tem suporte apenas quando o decodificador está agindo como um DMO (objeto de mídia do DirectX). Não há suporte para nenhuma dobra de nenhum tipo quando o decodificador está agindo como uma Media Foundation transformação (MFT).

No Windows Vista, se você obtiver uma interface **IPropertyStore** em um decodificador de áudio, o decodificador atuará como um MFT. Consequentemente, essa propriedade não pode ser usada no Windows Vista. Para obter informações sobre quando um decodificador atua como um DMO ou uma MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).

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

 

 
