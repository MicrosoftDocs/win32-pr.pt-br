---
title: Configuração do registro da DLL de administração do RAS
description: Entenda os requisitos para registrar uma DLL de administração de serviço de acesso remoto (RAS) de terceiros com o RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406709"
---
# <a name="ras-administration-dll-registry-setup"></a>Configuração do registro da DLL de administração do RAS

O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar a DLL, defina os valores a seguir nessa chave.



| Nome do valor    | Dados do valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll. |
| *DLLPath*     | Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.                  |



 

Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc. pode ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **reg \_ sz** : dll de administração de Ras proeletromagnético

*DLLPath* : **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll

O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção/desinstalação. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro da DLL.

 

 




