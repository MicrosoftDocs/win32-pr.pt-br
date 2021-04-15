---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461184"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>\_Propriedade MF CONTENTDECRYPTIONMODULE \_ caminhodearmazenamento

Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.


## <a name="data-type"></a>Tipo de dados

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID da propriedade

**\_CONTENTDECRYPTIONMODULE MF \_ caminhodearmazenamento**

## <a name="property-value"></a>Valor da propriedade

Um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.

## <a name="remarks"></a>Comentários

O caminho especificado com essa propriedade também será usado para dados específicos de conteúdo se a propriedade [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) não estiver definida.

Para melhorar o desempenho COM, o aplicativo não deve excluir o local do repositório após o lançamento do objeto CDM.



Defina essa propriedade ao criar um CDM chamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Atualização de abril de 2020 do Windows 10<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Confira também

- [Propriedades de Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




