---
title: Tipos de exclusão mútua
description: Tipos de exclusão mútua
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- SDK do Windows Media Format, exclusão mútua
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- exclusão mútua, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007072"
---
# <a name="mutual-exclusion-types"></a>Tipos de exclusão mútua

Você pode usar tipos de exclusão mútua para identificar a natureza de um objeto de exclusão mútua em um perfil. Os tipos de exclusão mútua são usados como parâmetros para [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).

A tabela a seguir lista os identificadores para tipos de exclusão mútua.



| Constante de tipo de exclusão mútua | GUID                                 |
|--------------------------------|--------------------------------------|
| \_Linguagem WMMUTEX do CLSID \_       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| \_Taxa de \_ bits WMMUTEX CLSID        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| Apresentação do CLSID \_ WMMUTEX \_   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ desconhecido        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Valores GUID**](guid-values.md)
</dt> </dl>

 

 




