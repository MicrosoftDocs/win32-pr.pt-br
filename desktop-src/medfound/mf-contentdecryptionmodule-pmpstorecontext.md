---
description: Especifica uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM) que usam MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798318"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>\_Propriedade MF CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT

Especifica uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM) que usam [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Tipo de dados

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID da propriedade

**\_CONTENTDECRYPTIONMODULE MF \_ PMPSTORECONTEXT**

## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM).

## <a name="remarks"></a>Comentários

O implementador CDM deve procurar esse valor e passar o valor para o [Construtor MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) usando o nome da propriedade "Windows. Media. Protection. PMPStoreContext".


Os aplicativos não devem criar essa propriedade ao chamar [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Atualização de abril de 2020 do Windows 10<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Confira também

- [Propriedades de Media Foundation](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




