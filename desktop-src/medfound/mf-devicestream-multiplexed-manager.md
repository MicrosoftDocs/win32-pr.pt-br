---
description: Fornece uma instância de IMFMuxStreamAttributesManager que gerencia o IMFAttributes que descreve os subfluxos de uma fonte de mídia multiplexada.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Atributo MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748878"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>\_Atributo de \_ Gerenciador de multiplexado de DEVICESTREAM MF \_

Fornece uma instância de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) que gerencia o [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) que descreve os subfluxos de uma fonte de mídia multiplexada.

## <a name="data-type"></a>Tipo de dados

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Comentários

Passe esse valor em [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para determinar se a origem da mídia fornece fluxos multiplexados e, nesse caso, obter uma instância de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
