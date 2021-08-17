---
description: Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixação na barra de tarefas ou para inclusão na lista MFU (mais usada) do menu Iniciar.
title: Como excluir itens da pinagem da barra de tarefas e listas recentes/frequentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3adb60353836e436f4327837c30448c7628a435048cc2a41b0464d56341f410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223560"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Como excluir itens da pinagem da barra de tarefas e listas recentes/frequentes

Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixar na barra de tarefas ou para inclusão na lista MFU (Uso Mais Usado) do **menu** Iniciar.

## <a name="instructions"></a>Instruções


Há três mecanismos para realizar a exclusão de itens da pinagem da barra de tarefas e listas recentes/frequentes:

-   Adicione a entrada NoStartPage ao registro do aplicativo, conforme mostrado neste exemplo:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Os dados associados à entrada NoStartPage são ignorados. Somente a presença da entrada é necessária. Portanto, o tipo ideal para NoStartPage é **REG \_ NONE.**

    Observe que qualquer uso de uma ID explícita do Modelo de Usuário do Aplicativo (AppUserModelID) substitui a entrada NoStartPage. Se um AppUserModelID explícito for aplicado a um atalho, processo ou janela, ele se tornará fixável e qualificado para a lista MFU **do** menu Iniciar.

-   Defina [a propriedade System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) em janelas e atalhos. Essa propriedade deve ser definida em uma janela antes que a propriedade [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) seja definida.
-   Adicione um AppUserModelID explícito como um valor sob a seguinte sub-chave do Registro, conforme mostrado neste exemplo:

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

    Cada entrada é **um valor REG \_ NULL** com o nome do AppUserModelID. Qualquer AppUserModelID encontrado nesta lista não é fixável e não está qualificado para inclusão na lista MFU **do** menu Iniciar.

## <a name="remarks"></a>Comentários

Esteja ciente de que determinados arquivos executáveis, bem como atalhos que contêm determinadas cadeias de caracteres em seus nomes, são excluídos automaticamente da fixar e incluir na lista MFU.

> [!Note]  
> Essa exclusão automática pode ser substituído aplicando um AppUserModelID explícito.

 

Se qualquer uma das cadeias de caracteres a seguir, independentemente do caso, estiver incluída no nome do atalho, o programa não será fixável e não será exibido na lista usada com mais frequência (não aplicável ao Windows 10):

-   Documentação
-   Ajuda
-   Instalar
-   Mais informações
-   Leia-me
-   Ler primeiro
-   Leiame
-   Remover
-   Instalação
-   Suporte
-   What's New

A lista de programas a seguir não é fixável e são excluídos da lista usada com mais frequência:

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

As listas anteriores são armazenadas nos valores do Registro a seguir.

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

 

 
