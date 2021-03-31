---
description: Define a configuração de fluxo para a origem de mídia WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Propriedade MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921393"
---
# <a name="mfpkey_sbesourcemode-property"></a>\_Propriedade MFPKEY SBESourceMode

Define a configuração de fluxo para a origem de mídia WTV.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**INT**

VT \_ int

**intVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a origem da mídia WTV. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

A origem de mídia do WTV lê arquivos de TV gravados do Windows (. wtv e. ms-drv).

Essa propriedade deve ter um dos valores a seguir.

-   1: mapear os fluxos de áudio disponíveis para uma única saída, com base no local do sistema. Esse modo é apropriado para reprodução. (Padrão.)
-   2. Todos os fluxos de áudio e subfluxos (como a legenda e os fluxos de dados) são selecionados. Esse modo é apropriado para remuxing ou transcodificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
