---
description: Ilustra a invocação de um comando DDE usando um verbo do Shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Como associar verbos a comandos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216cfca1548ed16dfea2f018fc3a1607d5c29d080f0f54541ace0491813a73d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090576"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Como associar verbos a comandos DDE

Invocar um verbo normalmente inicia o aplicativo que é especificado pela subchave de comando do verbo. no entanto, se seu aplicativo der suporte a troca dinâmica de dados (DDE), você poderá fazer com que o Shell inicie uma conversa DDE.

Para especificar que a invocação de um verbo deve iniciar uma conversa DDE, siga estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Adicione uma subchave **ddeexec** à chave do verbo.

### <a name="step-2"></a>Etapa 2:

Defina o valor padrão de **ddeexec** para a cadeia de caracteres de comando DDE.

## <a name="remarks"></a>Comentários

A chave **ddeexec** tem três subchaves opcionais que fornecem algum controle sobre o processo DDE:

-   **aplicativo**. Defina o valor padrão dessa subchave como o nome do aplicativo a ser usado para estabelecer a conversa DDE. Se não houver nenhuma subchave de **aplicativo** , o valor padrão da subchave de **comando** do verbo será usado como o nome do aplicativo.
-   **tópico**. Defina o valor padrão dessa subchave como o nome do tópico da conversa DDE. Se não houver subchave de **tópico** , o sistema será usado como o nome do tópico.
-   **ifexec**. Defina o valor padrão dessa subchave como o comando DDE a ser usado se a conversa DDE não puder ser iniciada. Quando a inicialização falha, o aplicativo especificado pelo valor padrão da subchave de **comando** do verbo é iniciado. Se existir uma chave **ifexec** , seu valor padrão será usado como o comando DDE. Se não houver nenhuma subchave **ifexec** , o valor padrão da chave **ddeexec** será usado novamente como o comando DDE.

O exemplo a seguir especifica que invocar o verbo Open para myprogram. 1 inicia uma conversa DDE com um comando DDE aberto ("%1") e um nome de aplicativo de myprogram.

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



