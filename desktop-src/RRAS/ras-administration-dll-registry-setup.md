---
title: Sobre a configuração do registro da DLL de administração do RAS
description: Entenda os requisitos para registrar uma DLL de administração de serviço de acesso remoto (RAS) de terceiros com o RAS. O RAS dá suporte a várias DLLs de administração de RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Administração de RAS RRAS, configuração do registro de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406659"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Sobre a configuração do registro da DLL de administração do RAS

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



 

Como o RAS dá suporte a várias DLLs de administração de RAS, o valor de registro **DLLPath** pode conter uma lista delimitada por ponto-e-vírgula de caminhos. Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc., pode ser a seguinte:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ sz** : dll de administração de Ras proeletromagnético

*DLLPath*: **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll; C: \\ NT \\ System32 \\ntwkadm2.dll

O RAS chama as DLLs na ordem em que estão listadas nesse valor de registro. O valor *DisplayName* do registro ainda contém apenas um único nome de exibição.

O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção e desinstalação. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro para a DLL.

**Windows 2000/NT:** O RAS dá suporte a apenas uma DLL de administração de RAS, portanto, o valor de registro **DLLPath** não pode conter uma lista delimitada por ponto-e-vírgula de caminhos.

 

 




