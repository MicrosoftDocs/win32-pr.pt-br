---
description: Define o modo de processamento para o DSP de Captura de Voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973265"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE

Define o modo de processamento para o DSP de Captura de Voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da [enumeração AEC \_ SYSTEM \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

A propriedade deve ser um dos valores a seguir.



| Valor | Descrição                                 |
|-------|---------------------------------------------|
| 0     | Modo somente AEC (cancelamento de eco de áudio)     |
| 2     | Modo somente MAP (processamento de matriz de microfone) |
| 4     | Modo AEC e MAP                            |
| 5     | Nem o modo AEC nem MAP                    |



 

Você deve definir essa propriedade antes de usar o DSP de Captura de Voz. Depois de definir essa propriedade, você pode usar o DSP com suas configurações padrão ou definir propriedades adicionais.

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

 

 
