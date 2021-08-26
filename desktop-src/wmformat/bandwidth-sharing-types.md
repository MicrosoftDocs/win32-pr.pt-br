---
title: Tipos de compartilhamento de largura de banda
description: Tipos de compartilhamento de largura de banda
ms.assetid: 2da15981-65d4-4d77-a68c-810ded18670c
keywords:
- Windows SDK de Formato de Mídia, compartilhamento de largura de banda
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (Formato de Sistemas Avançados), compartilhamento de largura de banda
- compartilhamento de largura de banda, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2b9ea05210e39c54334373be725284dbd1affc0170be6568600eeb4c2bead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055586"
---
# <a name="bandwidth-sharing-types"></a>Tipos de compartilhamento de largura de banda

Você pode usar tipos de compartilhamento de largura de banda para identificar a natureza de um objeto de compartilhamento de largura de banda em um perfil. Os tipos de compartilhamento de largura de banda são usados como parâmetros [**para IWMBandwidthSharing::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype) e [**IWMBandwidthSharing::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype).

A tabela a seguir lista os identificadores para tipos de compartilhamento de largura de banda.



| Constante de tipo de compartilhamento de largura de banda      | GUID                                 |
|--------------------------------------|--------------------------------------|
| CLSID \_ WMBandwidthSharing \_ Exclusivo | af6060aa-5197-11d2-b6af-00c04fd908e9 |
| CLSID \_ WMBandwidthSharing \_ Parcial   | af6060ab-5197-11d2-b6af-00c04fd908e9 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Valores de GUID**](guid-values.md)
</dt> </dl>

 

 




