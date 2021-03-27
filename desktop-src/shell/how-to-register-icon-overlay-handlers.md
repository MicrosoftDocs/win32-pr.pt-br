---
description: Além do registro COM (normal Component Object Model), as etapas a seguir devem ser concluídas para registrar manipuladores de sobreposição de ícone.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Como registrar manipuladores de sobreposição de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988977"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Como registrar manipuladores de sobreposição de ícone

Além do registro COM (normal Component Object Model), as etapas a seguir devem ser concluídas para registrar manipuladores de sobreposição de ícone.

## <a name="instructions"></a>Instruções

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Etapa 1: criar uma subchave chamada para o manipulador sob essa chave

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Etapa 2: definir o valor padrão da subchave para a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do objeto

O exemplo a seguir ilustra como registrar um manipulador de sobreposição de ícone chamado myoverlay.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



