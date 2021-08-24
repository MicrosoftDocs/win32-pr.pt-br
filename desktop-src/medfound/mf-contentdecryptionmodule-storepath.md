---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o CDM (Módulo de Descriptografia de Conteúdo) pode usar para inicialização.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8126bfea15f9946bb9950293a6c39c101f9c37c8870176fb4bb0108aa5862bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723456"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>Propriedade \_ STOREPATH CONTENTDECRYPTIONMODULE \_ MF

Especifica um caminho de arquivo que representa um local de armazenamento que o CDM (Módulo de Descriptografia de Conteúdo) pode usar para inicialização.


## <a name="data-type"></a>Tipo de dados

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID da propriedade

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valor da propriedade

Um caminho de arquivo que representa um local de armazenamento que o CDM (Módulo de Descriptografia de Conteúdo) pode usar para inicialização.

## <a name="remarks"></a>Comentários

O caminho especificado com essa propriedade também será usado para dados específicos do conteúdo se a [propriedade MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) não estiver definida.

Para melhorar o desempenho do COM, o aplicativo não deve excluir o local da loja depois que o objeto CDM tiver sido liberado.



De definir essa propriedade ao criar um CDM chamando [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 Atualização de abril de 2020<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Confira também

- [Media Foundation propriedades](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




