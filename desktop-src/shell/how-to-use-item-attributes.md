---
description: Os valores de sinalizador SFGAO dos atributos do Shell para um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Como usar atributos de item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ddcc567a820ba1d9c1394ca38f78fc9ce9ec634596f8dbe41feca9def32e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859565"
---
# <a name="how-to-use-item-attributes"></a>Como usar atributos de item

Os [**valores de sinalizador SFGAO**](sfgao.md) dos atributos do Shell para um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.

Para usar esse recurso de atributo, adicione os seguintes **valores REG \_ DWORD** sob o verbo:

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

O valor AttributeMask especifica o [**valor de SFGAO**](sfgao.md) dos valores de bit da máscara com o que testar.

### <a name="step-2"></a>Etapa 2:

O valor AttributeValue especifica o [**valor SFGAO**](sfgao.md) dos bits testados.

### <a name="step-3"></a>Etapa 3:

O ImpliedSelectionModel especifica zero para verbos de item ou diferente de zero para verbos no menu de atalho de plano de fundo.

## <a name="remarks"></a>Comentários

Na entrada de registro de exemplo a seguir, AttributeMask é definido como [**SFGAO \_ READONLY**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



