---
title: Configuração do Registro de DLL de Administração ras
description: Entenda os requisitos para registrar uma DLL de administração ras (serviço de acesso remoto) de terceiros com RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e40ed8fe4fe853c12e33e6168cb72cf1b3ec5b33afc92e8767731a13ec37412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036356"
---
# <a name="ras-administration-dll-registry-setup"></a>Configuração do Registro de DLL de Administração ras

O programa de instalação para uma DLL de administração RAS de terceiros deve registrar a DLL com RAS fornecendo informações na chave a seguir no Registro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar a DLL, deverão ser definidos os valores a seguir nessa chave.



| Nome do valor    | Dados do valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Uma **cadeia \_ de caracteres REG SZ** que contém o nome de exibição amigável da DLL. |
| *DLLPath*     | Uma **cadeia \_ de caracteres REG SZ** que contém o caminho completo da DLL.                  |



 

Por exemplo, a entrada do Registro para uma DLL de administração ras de uma empresa fictícia chamada ProElectron, Inc. pode ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName:* **REG \_ SZ:** DLL de administrador ras proelectron

*DLLPath:* **REG \_ SZ:** C: \\ nt \\ system32 \\ntwkadm.dll

O programa de instalação para uma DLL de administração ras também deve fornecer a funcionalidade remover/desinstalar. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do Registro da DLL.

 

 




