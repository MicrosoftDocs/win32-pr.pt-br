---
description: Contém um ponteiro para a interface de retorno de chamada IMFNetResourceFilter para o fluxo de bytes HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Propriedade MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661571"
---
# <a name="mfnetsource_resource_filter-property"></a>Propriedade de filtro de \_ recursos MFNETSOURCE \_

Contém um ponteiro para a interface de retorno de chamada [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) para o fluxo de bytes http Microsoft Media Foundation.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**IUnknown \** _

VT \_ desconhecido

_ *punkVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP. Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
