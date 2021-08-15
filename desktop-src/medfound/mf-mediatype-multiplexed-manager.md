---
description: Fornece uma instância de IMFMuxStreamMediaTypeManager que pode ser usada para obter os tipos de mídia dos subfluxos de uma fonte de mídia multiplexada, bem como controlar a combinação de subfluxos que são multiplexados pela origem.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Atributo MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe00e8824997a0af89099c7fbaad4a2378b44c3360bad0d4b8808023355da2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973685"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>\_Atributo do \_ Gerenciador de MediaType do MF \_

Fornece uma instância de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) que pode ser usada para obter os tipos de mídia dos subfluxos de uma fonte de mídia multiplexada, bem como controlar a combinação de subfluxos que são multiplexados pela origem.

## <a name="data-type"></a>Tipo de dados

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Comentários

Passe esse valor em [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obter uma instância de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
