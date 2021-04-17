---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501938"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>\_Propriedade MF CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH

Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.


## <a name="data-type"></a>Tipo de dados

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID da propriedade

**\_CONTENTDECRYPTIONMODULE MF \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Valor da propriedade

Um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.

## <a name="remarks"></a>Comentários

O aplicativo deve excluir o local do repositório após o lançamento do objeto CDM.

Se essa propriedade não estiver definida, o sistema usará o caminho especificado com a propriedade [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) para dados específicos de conteúdo.

Defina essa propriedade ao criar um CDM chamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Atualização de abril de 2020 do Windows 10<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Confira também

- [Propriedades de Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




