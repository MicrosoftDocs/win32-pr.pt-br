---
title: Registrando uma DLL de segurança RAS
description: O programa de instalação para uma DLL de segurança RAS deve registrar a DLL com o servidor RAS do Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635688"
---
# <a name="registering-a-ras-security-dll"></a>Registrando uma DLL de segurança RAS

O programa de instalação para uma DLL de segurança RAS deve registrar a DLL com o servidor RAS do Windows NT/Windows 2000. Somente uma DLL de segurança RAS pode ser registrada como suporte para várias DLLs de segurança não é fornecida. Para registrar uma DLL de segurança de RAS, defina o valor de *DLLPath* sob a seguinte chave no registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nome do valor | Dados do valor                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Uma cadeia de caracteres **reg \_ sz** que contém o caminho da dll. Essa cadeia de caracteres deve especificar o caminho completo, a menos que a DLL esteja em um diretório listado no caminho do sistema. |



 

O programa de instalação para uma DLL de segurança de RAS também deve fornecer a funcionalidade de remoção/desinstalação. Se um usuário remover a DLL, o programa de instalação deverá excluir o valor de *DLLPath* do registro. O serviço RAS não será iniciado se o valor de *DLLPath* especificar uma DLL que não pode ser encontrada.

Uma DLL de segurança RAS deve exportar as funções [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) e [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .

 

 




