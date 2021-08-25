---
title: Sobre a Instalação do Registro de DLL de Administração ras
description: Entenda os requisitos para registrar uma DLL de administração ras (serviço de acesso remoto) de terceiros com RAS. O RAS dá suporte a várias DLLs de Administração rasa.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RRAS de Administração ras, configuração do registro DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dbabc7a667455bce2cffbd3d04591076f820efa755c0f512f27130a82fde4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909906"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Sobre a Instalação do Registro de DLL de Administração ras

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



 

Como o RAS dá suporte a várias DLLs de administração RAS, o valor do Registro **DLLPath** pode conter uma lista delimitada por pontos e vírgulas de caminhos. Por exemplo, a entrada do Registro para uma DLL de administração ras de uma empresa fictícia chamada ProElectron, Inc., pode ser a seguinte:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName:* **REG \_ SZ:** DLL de administrador ras proelectron

*DLLPath:* **REG \_ SZ:** C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS chama as DLLs na ordem em que estão listadas neste valor do Registro. O valor do Registro *DisplayName* ainda contém apenas um único nome de exibição.

O programa de instalação para uma DLL de administração ras também deve fornecer a funcionalidade remover e desinstalar. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do Registro para a DLL.

**Windows 2000/NT:** O RAS dá suporte a apenas uma DLL de Administração RAS, portanto, o valor do Registro **DLLPath** não pode conter uma lista delimitada por pontos e vírgulas de caminhos.

 

 




