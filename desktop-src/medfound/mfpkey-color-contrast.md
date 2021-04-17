---
description: Ajusta o contraste.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Propriedade MFPKEY_COLOR_CONTRAST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785169"
---
# <a name="mfpkey_color_contrast-property"></a>\_Propriedade contraste de cor do MFPKEY \_

Ajusta o contraste.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de transformação de controle de cores](colorcontroltransform.md)

## <a name="remarks"></a>Comentários

O ajuste de contraste é executado multiplicando os valores de YCbCr por um fator de dimensionamento.

Essa propriedade tem um intervalo de-127 a 127. Zero indica que não há alteração em contraste.

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

 

 
