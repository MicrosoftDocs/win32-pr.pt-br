---
description: Define o modo de processamento para o DSP de captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Propriedade MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764716"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>\_Propriedade do \_ modo do sistema MFPKEY WMAAECMA \_

Define o modo de processamento para o DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo do sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

A propriedade deve ser um dos valores a seguir.



| Valor | Descrição                                 |
|-------|---------------------------------------------|
| 0     | Modo somente do AEC (cancelamento de eco de áudio)     |
| 2     | Modo somente de processamento de matriz de microfone (MAP) |
| 4     | AEC e modo de mapa                            |
| 5     | Nenhum AEC nem modo de mapa                    |



 

Você deve definir essa propriedade antes de usar o DSP de captura de voz. Depois de definir essa propriedade, você pode usar o DSP com suas configurações padrão ou definir propriedades adicionais.

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

 

 
