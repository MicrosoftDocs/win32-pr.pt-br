---
description: Além do registro COM (normal Component Object Model), as etapas a seguir devem ser concluídas para registrar manipuladores de sobreposição de ícone.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Como registrar manipuladores de sobreposição de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0e62d95b224b131f03c2bd976ddf7c01d7cb3de7ad6995f21568dc7e990d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714906"
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

 

 



