---
description: Para adicionar um item ao submenu programas, siga estas etapas.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Como adicionar atalhos ao menu iniciar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091611"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Como adicionar atalhos ao menu iniciar

Para adicionar um item ao submenu **programas** , siga estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie um [link do Shell](./links.md) usando a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .

### <a name="step-2"></a>Etapa 2:

Obtenha o local da pasta programas usando a função [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , passando os [**\_ programas FolderId**](knownfolderid.md).

### <a name="step-3"></a>Etapa 3:

Adicione o link do Shell à pasta programas. Você também pode criar uma pasta na pasta programas e adicionar o link a essa pasta.

 

 
