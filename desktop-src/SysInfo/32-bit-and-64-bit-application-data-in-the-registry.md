---
description: No Windows de 64 bits, partes das entradas do registro são armazenadas separadamente para aplicativos de 32 bits e de 64 bits e mapeadas em exibições lógicas separadas do registro usando o redirecionador do registro e a reflexão do registro, pois a versão de 64 bits de um aplicativo pode usar chaves de registro e valores diferentes da versão de 32 bits. Também há chaves de registro compartilhadas que não são redirecionadas ou refletidas.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dados de aplicativo de 32 bits e 64 bits no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828528"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Dados de aplicativo de 32 bits e 64 bits no registro

No Windows de 64 bits, partes das entradas do registro são armazenadas separadamente para aplicativos de 32 bits e de 64 bits e mapeadas em exibições lógicas separadas do registro usando o [redirecionador do registro](/windows/desktop/WinProg64/registry-redirector) e a [reflexão do registro](/windows/desktop/WinProg64/registry-reflection), pois a versão de 64 bits de um aplicativo pode usar chaves de registro e valores diferentes da versão de 32 bits. Também há [chaves de registro compartilhadas](/windows/desktop/WinProg64/shared-registry-keys) que não são redirecionadas ou refletidas.

O pai de cada nó de registro de 64 bits é o Image-Specific nó ou não. O redirecionador de registro direciona, de forma transparente, o acesso de registro de um aplicativo ao subnó não apropriado. Os subnós de redirecionamento na árvore do registro são criados automaticamente pelo componente WOW64 usando o nome **Wow6432Node**. Como resultado, é essencial não nomear nenhuma chave do registro que você criar **Wow6432Node**.

Os principais \_ \_ sinalizadores 64KEY de WOW64 \_ e \_ 32KEY da chave WOW64 habilitam o acesso explícito à exibição do registro de 64 bits e à exibição de 32 bits, respectivamente. Para obter mais informações, consulte [acessando uma exibição de registro alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Para desabilitar e habilitar a reflexão do registro para uma chave específica, use as funções [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) . Os aplicativos devem desabilitar a reflexão somente para as chaves do registro que elas criam e não tentar desabilitar a reflexão para as chaves predefinidas, como **HKEY \_ local \_ Machine** ou **HKEY \_ Current \_ User**. Para determinar quais chaves estão na lista de reflexo, use a função [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de registro](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[reflexão do registro](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
