---
description: O método SelectDefaultSubpictureLanguage define a linguagem de subimagem padrão atual no objeto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Método SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aaa6b927d33626299258ac54136e1a67b0dedb40427a35d9c79465be3e9a15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072580"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Método SelectDefaultSubpictureLanguage

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SelectDefaultSubpictureLanguage` método define a linguagem de subimagem padrão atual no objeto **MSWebDVD** .

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Especifica o idioma como um inteiro.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Especifica a extensão de linguagem da subimagem como um inteiro.



| Valor | Descrição                    |
|-------|--------------------------------|
| 0     | Extensão não especificada        |
| 1     | Legendas normais                |
| 2     | Legendas grandes                   |
| 3     | Legendas das crianças            |
| 5     | Legendas normais ocultas         |
| 6     | Legendas grandes ocultas            |
| 7     | Legendas ocultas de filhos     |
| 9     | Forced (forçado)                         |
| 13    | Comentários do diretor normal     |
| 14    | Comentários do Big Director        |
| 15    | Comentários de Director's dos filhos |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A extensão de linguagem de subimagem fornece mais informações sobre a subimagem.

 

 



