---
description: Especifica o final de uma passagem de codificação.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977c876d14c6757c5f1bc31e0d5b7cc58f6e13fad827cc23f821be8382a5e376
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738183"
---
# <a name="mfpkey_endofpass-property"></a>Propriedade MFPKEY \_ ENDOFPASS

Especifica o final de uma passagem de codificação.

## <a name="data-type"></a>Tipo de Dados

**BOOL da VT \_**

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo de dados para IPropertyBag

Nenhum tipo de dados é necessário. Para definir essa propriedade, passe uma VARIANT não **reinicializada.**

## <a name="remarks"></a>Comentários

Essa propriedade não é uma propriedade normal porque tem o mesmo efeito, independentemente de o valor ser VARIANT \_ TRUE ou VARIANT \_ FALSE. Você deve definir essa propriedade depois de processar os últimos exemplos de entrada para uma passagem de pré-processamento. Se você estiver executando várias passagens, deverá definir essa propriedade no final de cada passagem de pré-processamento (no momento, nenhum dos codecs dá suporte a mais de um). Se você não definir essa propriedade, o codec assumirá que você ainda está passando amostras para pré-processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




