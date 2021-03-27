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
# <a name="how-to-register-icon-overlay-handlers"></a><span data-ttu-id="7d5b9-103">Como registrar manipuladores de sobreposição de ícone</span><span class="sxs-lookup"><span data-stu-id="7d5b9-103">How to Register Icon Overlay Handlers</span></span>

<span data-ttu-id="7d5b9-104">Além do registro COM (normal Component Object Model), as etapas a seguir devem ser concluídas para registrar manipuladores de sobreposição de ícone.</span><span class="sxs-lookup"><span data-stu-id="7d5b9-104">In addition to normal Component Object Model (COM) registration, the following steps must be completed in order to register icon overlay handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="7d5b9-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="7d5b9-105">Instructions</span></span>

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a><span data-ttu-id="7d5b9-106">Etapa 1: criar uma subchave chamada para o manipulador sob essa chave</span><span class="sxs-lookup"><span data-stu-id="7d5b9-106">Step 1: Create a subkey named for the handler under this key</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a><span data-ttu-id="7d5b9-107">Etapa 2: definir o valor padrão da subchave para a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do objeto</span><span class="sxs-lookup"><span data-stu-id="7d5b9-107">Step 2: Set the default value of the subkey to the string form of the object's class identifier (CLSID)GUID</span></span>

<span data-ttu-id="7d5b9-108">O exemplo a seguir ilustra como registrar um manipulador de sobreposição de ícone chamado myoverlay.</span><span class="sxs-lookup"><span data-stu-id="7d5b9-108">The following example illustrates how to register an icon overlay handler named MyOverlay.</span></span>

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

 

 



