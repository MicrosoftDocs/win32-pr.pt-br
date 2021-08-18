---
description: Define a configuração de fluxo para a fonte de mídia da WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973365"
---
# <a name="mfpkey_sbesourcemode-property"></a>Propriedade \_ MFPKEY SBESourceMode

Define a configuração de fluxo para a fonte de mídia da WTV.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a fonte de mídia da WTV. Para definir a propriedade , passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

A fonte de mídia da WTV Windows arquivos tv show gravados (.wtv e .ms-drv).

Essa propriedade deve ter um dos valores a seguir.

-   1: Mapeie os fluxos de áudio disponíveis para uma única saída, com base no local do sistema. Esse modo é apropriado para reprodução. (Padrão.)
-   2. Todos os fluxos de áudio e substreams (como legenda e fluxos de dados) são selecionados. Esse modo é apropriado para remuxing ou transcodificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
