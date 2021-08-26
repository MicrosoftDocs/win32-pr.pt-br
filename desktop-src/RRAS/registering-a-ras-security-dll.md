---
title: Registrando uma DLL de segurança RAS
description: o programa de instalação para uma DLL de segurança RAS deve registrar a dll com o servidor RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5ca32aa687649c80917f9a072b9d4cbeb0f1f4e8ba61ce090e7781bb04cdefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028406"
---
# <a name="registering-a-ras-security-dll"></a>Registrando uma DLL de segurança RAS

o programa de instalação para uma DLL de segurança RAS deve registrar a dll com o servidor RAS Windows NT/Windows 2000. Somente uma DLL de segurança RAS pode ser registrada como suporte para várias DLLs de segurança não é fornecida. Para registrar uma DLL de segurança de RAS, defina o valor de *DLLPath* sob a seguinte chave no registro:

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

 

 




