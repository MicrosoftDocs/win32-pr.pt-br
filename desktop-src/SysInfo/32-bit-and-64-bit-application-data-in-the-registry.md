---
description: No Windows de 64 bits, partes das entradas do Registro são armazenadas separadamente para aplicativos de 32 bits e aplicativos de 64 bits e mapeadas em exibições de registro lógico separadas usando o redirecionador do Registro e a reflexão do Registro, pois a versão de 64 bits de um aplicativo pode usar chaves e valores do Registro diferentes da versão de 32 bits. Também há chaves de Registro compartilhadas que não são redirecionadas nem refletidas.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dados de aplicativo de 32 bits e 64 bits no Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d5177eb48a5497e321b47bb0da96874a0e6522360f2dc519dc72df3dcdf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764979"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Dados de aplicativo de 32 bits e 64 bits no Registro

No Windows de 64 bits, partes das entradas do Registro são armazenadas separadamente para aplicativos de 32 bits e aplicativos de 64 bits e mapeadas em exibições de registro lógico separadas usando o redirecionador do Registro e a reflexão do [Registro,](/windows/desktop/WinProg64/registry-reflection)pois a versão de 64 bits de um aplicativo pode usar chaves e valores do Registro diferentes da versão de 32 bits. [](/windows/desktop/WinProg64/registry-redirector) Também há chaves [de Registro compartilhadas](/windows/desktop/WinProg64/shared-registry-keys) que não são redirecionadas nem refletidas.

O pai de cada nó do Registro de 64 bits é o nó Image-Specific ou ISN. O redirecionador de registro direciona de forma transparente o acesso do Registro de um aplicativo ao subnónodo ISN apropriado. Os subnónodos de redirecionamento na árvore do Registro são criados automaticamente pelo componente WOW64 usando o nome **Wow6432Node**. Como resultado, é essencial não nomear nenhuma chave do Registro que você criar **wow6432Node.**

Os sinalizadores KEY \_ WOW64 64KEY e KEY WOW64 32KEY permitem o acesso explícito à exibição do Registro de 64 bits e à exibição de \_ \_ \_ 32 bits, respectivamente. Para obter mais informações, [consulte Acessando uma exibição de registro alternativa.](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)

Para desabilitar e habilitar a reflexão do Registro para uma chave específica, use as funções [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey.**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) Os aplicativos devem desabilitar a reflexão somente para as chaves do Registro que criam e não tentar desabilitar a reflexão para as chaves predefinidos, como **HKEY \_ LOCAL \_ MACHINE** ou **HKEY \_ CURRENT \_ USER.** Para determinar quais chaves estão na lista de reflexão, use a [**função RegQueryReflectionKey.**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[redirecionador de registro](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[reflexão do registro](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
