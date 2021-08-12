---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244769"
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
| Cliente mínimo com suporte<br/> | Windows 10 Atualização de abril de 2020<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Veja também

- [Propriedades de Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




