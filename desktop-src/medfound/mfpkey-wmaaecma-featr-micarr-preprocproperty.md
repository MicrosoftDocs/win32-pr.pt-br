---
description: Especifica se o DSP de captura de voz executa o pré-processamento da matriz do microfone.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786166"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>\_ \_ \_ \_ Propriedade preproc MICARR do MFPKEY WMAAECMA

Especifica se o DSP de captura de voz executa o pré-processamento da matriz do microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ true

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O pré-processamento pode remover tons estacionários que interferem no processamento, como um tom com uma densidade fixa.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição            |
|----------------|------------------------|
| VARIANTE \_ falso | Desabilitar o pré-processamento. |
| VARIANTE \_ true  | Habilite o pré-processamento.  |



 

O valor padrão dessa propriedade é VARIANT \_ true (Enabled). Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
