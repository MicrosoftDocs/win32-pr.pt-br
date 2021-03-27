---
description: Ilustra como garantir que seu aplicativo aparece no menu abrir com e na caixa de diálogo para aplicativos da área de trabalho e está disponível como um aplicativo padrão da Windows Store para tipos de arquivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Como incluir um aplicativo na caixa de diálogo abrir com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828291"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Como incluir um aplicativo na caixa de diálogo abrir com

Ilustra como garantir que seu aplicativo aparece no menu **abrir com** e na caixa de diálogo para aplicativos da área de trabalho e está disponível como um aplicativo padrão da Windows Store para tipos de arquivo especificados.

## <a name="instructions"></a>Instruções

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Para cada tipo de arquivo, adicione seu aplicativo à subchave do registro OpenWithProgIds.

Adicione o ProgID como um nome de valor, com o tipo de valor de REG \_ None ou reg \_ sz e uma cadeia de caracteres vazia como o valor de dados.

Os exemplos de registro a seguir mostram entradas que associam o InfoPath e para Microsoft Visual Studio com o tipo de arquivo XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Comentários

A subchave **OpenWithProgids** é preferida para **OpenWithList** para identificar um aplicativo. Para obter mais informações sobre essas subchaves, consulte [definindo subchaves opcionais e atributos de extensão de tipo de arquivo](fa-file-types.md).

O **OpenWithList** é destinado apenas a aplicativos herdados (deve ser. exe somente) em sistemas operacionais anteriores ao Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



