---
title: Tipos de exclusão mútua
description: Tipos de exclusão mútua
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows SDK de Formato de Mídia, exclusão mútua
- ASF (Advanced Systems Format), exclusão mútua
- ASF (Formato de Sistemas Avançados), exclusão mútua
- exclusão mútua, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da546c753696144c68348c61d01473c7d6414290b5971c220ac8c983317b3b15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110266"
---
# <a name="mutual-exclusion-types"></a>Tipos de exclusão mútua

Você pode usar tipos de exclusão mútua para identificar a natureza de um objeto de exclusão mútua em um perfil. Os tipos de exclusão mútua são usados como parâmetros [**para IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion::SetType.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)

A tabela a seguir lista os identificadores para tipos de exclusão mútua.



| Constante de tipo de exclusão mútua | GUID                                 |
|--------------------------------|--------------------------------------|
| Linguagem \_ WMMUTEX CLSID \_       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| Taxa de bits WMMUTEX CLSID \_ \_        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ Presentation   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ Desconhecido        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Valores de GUID**](guid-values.md)
</dt> </dl>

 

 




