---
description: Obtém um objeto do tipo IMFCollection que contém objetos IMFSample que contêm NALUs (unidades de camada de abstração de rede) e unidades SEI (informações de aprimoramento complementar) encaminhadas por um decodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Atributo MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765151"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>\_Atributo MFSampleExtension ForwardedDecodeUnits

Obtém um objeto do tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contém objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contêm NALUs (unidades de camada de abstração de rede) e unidades sei (informações de aprimoramento complementar) encaminhadas por um decodificador.

## <a name="data-type"></a>Tipo de dados

**IUnknown**

## <a name="remarks"></a>Comentários

A coleção contém todas as unidades NALU/SEI personalizadas desde o quadro anterior com bytes de prevenção de emulação removidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




