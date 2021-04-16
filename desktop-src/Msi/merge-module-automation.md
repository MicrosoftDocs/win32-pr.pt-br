---
description: Mergemod.dll fornece um objeto COM que implementa operações de mesclagem e geração de imagem de origem para módulos de mesclagem. O objeto principal implementa interfaces para programas C/C++ e clientes de automação, incluindo Visual Basic e VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Mesclar automação de módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747540"
---
# <a name="merge-module-automation"></a>Mesclar automação de módulo

Mergemod.dll fornece um objeto COM que implementa operações de mesclagem e geração de imagem de origem para módulos de mesclagem. O objeto principal implementa interfaces para programas C/C++ e clientes de automação, incluindo Visual Basic e VBScript.

O método preferencial para instalar o Mergemod.dll é usando o Windows Installer. A ID do componente do componente que contém a interface COM do Mergemod.dll é {FD153241-37EC-11D2-8892-00A0C981B015}. O mesmo binário pode ser usado em todos os sistemas Windows e a dll se registrará automaticamente por meio do regsvr32 em sistemas mais antigos.

Observe que Mergemod.dll requer que o Msvcrt.dll seja instalado no sistema.

Observe que Mergemod.dll 2,0 é necessário para criar [módulos de mesclagem configuráveis](configurable-merge-modules.md). Mergemod.dll versão 2,0 fornece funcionalidade estendida no momento da compilação por meio da interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Esse CLSID dá suporte a todas as funcionalidades existentes da interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fornecida pelo Mergemod.dll versão 1,0. A interface padrão no objeto de [**mesclagem**](merge-object.md) do Mergemod.dll 2,0 é a interface **IMsmMerge2** em vez da interface **IMsmMerge** .

[Modelo de objeto para Mergemod.dll versão 1,0](object-model-for-mergemod-dll-version-1-0.md)

[Modelo de objeto para Mergemod.dll versão 2,0](object-model-for-mergemod-dll-version-2-0.md)

 

 
