---
description: Especifica o fim de uma passagem de codificação.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Propriedade MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827911"
---
# <a name="mfpkey_endofpass-property"></a>\_Propriedade MFPKEY ENDOFPASS

Especifica o fim de uma passagem de codificação.

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo de dados para IPropertyBag

Nenhum tipo de dados é necessário. Para definir essa propriedade, passe uma **variante** não inicializada.

## <a name="remarks"></a>Comentários

Essa propriedade não é uma propriedade normal porque tem o mesmo efeito, independentemente de o valor ser VARIANT \_ true ou Variant \_ false. Você deve definir essa propriedade depois de processar os últimos exemplos de entrada para uma passagem de pré-processamento. Se você estiver executando várias passagens, deverá definir essa propriedade no final de cada passagem de pré-processamento (no momento, nenhum dos codecs oferece suporte a mais de um). Se você não definir essa propriedade, o codec irá pressupor que você ainda está passando exemplos para pré-processamento.

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

 

 




