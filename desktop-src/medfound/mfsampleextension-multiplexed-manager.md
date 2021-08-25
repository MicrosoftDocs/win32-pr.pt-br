---
description: Fornece uma instância de IMFMuxStreamSampleManager, que é usada para acessar a coleção de amostras dos subfluxos de uma fonte de mídia multiplexada.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: Atributo MFSampleExtension_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848b613c4f6de9086f3da9636a29cad73499b7f0b37bd3445cee3d1086d61d7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848096"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a>\_Atributo de Gerenciador multiplexado MFSampleExtension \_

Fornece uma instância de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) , que é usada para acessar a coleção de amostras dos subfluxos de uma fonte de mídia multiplexada.

## <a name="data-type"></a>Tipo de dados

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Comentários

Passe esse valor em [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obter uma instância de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
