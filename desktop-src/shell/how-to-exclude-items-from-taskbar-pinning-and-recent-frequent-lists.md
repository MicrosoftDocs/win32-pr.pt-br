---
description: Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixação na barra de tarefas ou para inclusão na lista de uso mais frequente (MFU) do menu iniciar.
title: Como excluir itens da fixação da barra de tarefas e listas recentes/frequentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967903"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Como excluir itens da fixação da barra de tarefas e listas recentes/frequentes

Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixação na barra de tarefas ou para inclusão na lista de uso mais frequente (MFU) do menu **Iniciar** .

## <a name="instructions"></a>Instruções


Há três mecanismos para realizar a exclusão de itens da fixação da barra de tarefas e de listas recentes/frequentes:

-   Adicione a entrada NoStartPage ao registro do aplicativo, conforme mostrado neste exemplo:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Os dados associados à entrada NoStartPage são ignorados. Somente a presença da entrada é necessária. Portanto, o tipo ideal para NoStartPage é **reg \_ None**.

    Observe que qualquer uso de uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) substitui a entrada NoStartPage. Se um AppUserModelID explícito for aplicado a um atalho, processo ou janela, ele se tornará fixas e elegível para a lista MFU do menu **Iniciar** .

-   Defina a propriedade [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) no Windows e nos atalhos. Essa propriedade deve ser definida em uma janela antes de a propriedade de [ \_ \_ ID PKEY AppUserModel](../properties/props-system-appusermodel-id.md) ser definida.
-   Adicione um AppUserModelID explícito como um valor na seguinte subchave do registro, conforme mostrado neste exemplo:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Cada entrada é um **valor \_ nulo reg** com o nome do AppUserModelID. Qualquer AppUserModelID encontrado nessa lista não é fixas e não está qualificado para inclusão na lista de MFU do menu **Iniciar** .

## <a name="remarks"></a>Comentários

Lembre-se de que determinados arquivos executáveis, bem como os atalhos que contêm determinadas cadeias de caracteres em seus nomes, são excluídos automaticamente da fixação e inclusão na lista MFU.

> [!Note]  
> Essa exclusão automática pode ser substituída com a aplicação de um AppUserModelID explícito.

 

Se qualquer uma das cadeias de caracteres a seguir, independentemente do caso, estiver incluída no nome do atalho, o programa não será fixas e não será exibido na lista de usados com mais frequência (não aplicável ao Windows 10):

-   Documentação
-   Ajuda
-   Instalar
-   Mais informações
-   Leia-me
-   Leia primeiro
-   Leiame
-   Remover
-   Instalação
-   Suporte
-   What's New

A lista de programas a seguir não é fixas e é excluída da lista de usados com mais frequência:

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

As listas anteriores são armazenadas nos valores de registro a seguir.

> [!Note]  
> Essas listas não devem ser modificadas por aplicativos. Use um dos métodos de lista de exclusão descritos anteriormente neste tópico para a mesma experiência.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[A barra de tarefas](taskbar.md)
</dt> <dt>

[Extensões da barra de tarefas](taskbar-extensions.md)
</dt> </dl>

 

 
