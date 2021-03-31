---
title: UI_PKEY_LabelDescription
description: Identifica a \_ Propriedade PKEY LabelDescription da interface do usuário \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822767"
---
# <a name="ui_pkey_labeldescription"></a>\_LabelDescription PKEY \_ UI

Identifica a \_ Propriedade PKEY LabelDescription da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ LabelDescription é usada por um aplicativo para consultar a descrição associada a um [ \_ \_ rótulo de PKEY de interface do usuário](windowsribbon-reference-properties-uipkey-label.md).

O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.

 

O comprimento máximo é não associado.

Não há suporte para alinhamento à direita.

A captura de tela a seguir ilustra o uso de um rótulo e uma descrição de rótulo associada em um menu de aplicativo.

![captura de tela mostrando um rótulo e uma descrição de rótulo associada em um menu de aplicativo.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




