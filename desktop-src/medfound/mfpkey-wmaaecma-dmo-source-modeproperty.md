---
description: Especifica se o DSP de captura de voz usa modo de origem ou modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Propriedade MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164927"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>\_Propriedade do \_ \_ modo de origem MFPKEY WMAAECMA DMO \_

Especifica se o DSP de captura de voz usa modo de origem ou modo de filtro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ true

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

No modo de origem, o aplicativo não precisa enviar dados de entrada para o DSP, pois o DSP recebe automaticamente os dados dos dispositivos de áudio. No modo de filtro, o aplicativo deve enviar os dados de entrada para o DSP.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição  |
|----------------|--------------|
| VARIANTE \_ falso | Modo de filtro. |
| VARIANTE \_ true  | Modo de origem. |



 

> [!Note]  
> Quando o DMO está no modo de origem, você só deve chamar [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o formato de fluxo de saída e não chamar [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para definir formatos de fluxo de entrada. Caso contrário, a inicialização do DMO falhará.

 

Se o valor dessa propriedade for VARIANT \_ true, o DSP terá zero entradas. Se o valor for VARIANT \_ false, o DSP terá uma ou duas entradas, dependendo do valor da Propriedade do [modo do \_ \_ sistema MFPKEY \_ WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) , conforme mostrado na tabela a seguir.



| Valor                     | Número de entradas |
|---------------------------|------------------|
| OPTIBEAM \_ \_ de matriz e \_ AEC | 2                |
| \_somente matriz \_ OPTIBEAM     | 1                |
| \_AEC de canal único \_      | 2                |
| \_NSAGC de canal único \_    | 1                |



 

> [!Note]  
> Somente os modos com uma única entrada funcionarão com o filtro de wrapper DMO da API do DirectShow 9,0.

 

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

 

 
