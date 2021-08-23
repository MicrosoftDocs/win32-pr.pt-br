---
description: Especifica se o DSP de Captura de Voz usa o modo de origem ou o modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9dd01be5a020047410362b2fdfc27fd8d703a393e3ae2f557b1dd3a42bf80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555296"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE

Especifica se o DSP de Captura de Voz usa o modo de origem ou o modo de filtro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

VARIANT \_ TRUE

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

No modo de origem, o aplicativo não precisa enviar dados de entrada para o DSP, pois o DSP recebe dados automaticamente dos dispositivos de áudio. No modo de filtro, o aplicativo deve enviar os dados de entrada para o DSP.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição  |
|----------------|--------------|
| VARIANT \_ FALSE | Modo de filtro. |
| VARIANT \_ TRUE  | Modo de origem. |



 

> [!Note]  
> Quando o DMO estiver no modo de origem, você só deverá chamar [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o formato de fluxo de saída e não chamar [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para definir formatos de fluxo de entrada. Caso contrário DMO inicialização falhará.

 

Se o valor dessa propriedade for VARIANT \_ TRUE, o DSP terá zero entradas. Se o valor for VARIANT FALSE, o DSP terá uma ou duas entradas, dependendo do valor da propriedade \_ [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE,](mfpkey-wmaaecma-system-modeproperty.md) conforme mostrado na tabela a seguir.



| Valor                     | Número de entradas |
|---------------------------|------------------|
| OPT LTDAM \_ ARRAY \_ E \_ AEC | 2                |
| SOMENTE MATRIZ \_ OPTARGEMAM \_     | 1                |
| AEC \_ \_ DE CANAL ÚNICO      | 2                |
| \_ \_ NSAGC DE CANAL ÚNICO    | 1                |



 

> [!Note]  
> Somente os modos com uma única entrada funcionarão com o filtro wrapper DMO da API DirectShow 9.0.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
