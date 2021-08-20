---
description: Você pode usar o Registro para definir um ou mais verbos estendidos. Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto ao pressionar a tecla SHIFT.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Como definir verbos estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef73244a03101de02653625912701b81aa9e8e11d975f96dd417eaa137bfba07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859713"
---
# <a name="how-to-define-extended-verbs"></a>Como definir verbos estendidos

Você pode usar o Registro para definir um ou mais verbos estendidos. Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto ao pressionar a tecla SHIFT.

## <a name="instructions"></a>Instruções


Para definir um verbo como estendido, basta adicionar um valor **de REG \_ SZ** "estendido" à subkey do verbo. O valor não deve ter nenhum dado associado a ele. A entrada de registro de exemplo a seguir mostra o exemplo da seção anterior, com "doit" definido como um verbo estendido.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



