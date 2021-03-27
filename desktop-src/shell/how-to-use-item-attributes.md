---
description: Os valores de sinalizador SFGAO dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Como usar atributos de item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828286"
---
# <a name="how-to-use-item-attributes"></a>Como usar atributos de item

Os valores de sinalizador [**SFGAO**](sfgao.md) dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.

Para usar esse recurso de atributo, adicione os seguintes valores de **reg \_ DWORD** no verbo:

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

O valor AttributeMask especifica o valor de [**SFGAO**](sfgao.md) dos valores de bits da máscara com a qual testar.

### <a name="step-2"></a>Etapa 2:

O valor AttributeValue especifica o valor [**SFGAO**](sfgao.md) dos bits que são testados.

### <a name="step-3"></a>Etapa 3:

O ImpliedSelectionModel Especifica zero para verbos de item ou zero para verbos no menu de atalho de segundo plano.

## <a name="remarks"></a>Comentários

Na entrada de registro de exemplo a seguir, o AttributeMask é definido como [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

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

 

 



