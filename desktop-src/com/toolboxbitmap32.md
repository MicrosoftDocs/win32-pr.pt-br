---
title: ToolBoxBitmap32
description: Identifica o nome do módulo e a ID de recurso para um bitmap de 16 x 16 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005340"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Identifica o nome do módulo e a ID de recurso para um bitmap de 16 x 16 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz de reg** que especifica o nome do módulo e o identificador de recurso para o bitmap.

O tamanho do ícone padrão do Windows é muito grande para ser usado para essa finalidade. Isso requer contêineres de controle que têm um modo de design no qual um seleciona os controles e os coloca em um formulário que está sendo criado.

 

 




