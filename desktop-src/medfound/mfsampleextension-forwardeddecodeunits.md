---
description: Obtém um objeto do tipo IMFCollection que contém objetos IMFSample que contêm naLUs (unidades de camada de abstração de rede) e unidades SEI (Informações de Aprimoramento Suplementar) encaminhadas por um decodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713726"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>Atributo MFSampleExtension \_ ForwardedDecodeUnits

Obtém um objeto do tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contém objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contêm naLUs (unidades de camada de abstração de rede) e unidades SEI (Informações de Aprimoramento Suplementar) encaminhadas por um decodificador.

## <a name="data-type"></a>Tipo de dados

**IUnknown**

## <a name="remarks"></a>Comentários

A coleção contém todas as unidades NALU/SEI personalizadas desde o quadro anterior com bytes de prevenção de emulação removidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




