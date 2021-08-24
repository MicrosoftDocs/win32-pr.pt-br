---
description: Painel de Controle itens implementados em uma DLL que exporta a função CPlApplet têm requisitos de registro diferentes .exe arquivos.
title: Como registrar itens de Painel de Controle DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593186"
---
# <a name="how-to-register-dll-control-panel-items"></a>Como registrar itens de Painel de Controle DLL

> [!Note]  
> As diretrizes de implementação atuais Painel de Controle novos itens devem ser implementados como arquivos .exe em vez de .cpl arquivos. As informações a seguir são incluídas principalmente para fins herdado.

 

Painel de Controle itens implementados em uma DLL que exporta a [**função CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) têm requisitos de registro diferentes .exe arquivos. A partir Windows XP, novas DLLs de item de Painel de Controle devem ser instaladas na pasta do aplicativo associado na pasta Arquivos de Programas. Itens armazenados no diretório System32 com uma extensão .cpl não precisam ser registrados; eles são mostrados automaticamente no Painel de Controle. Todos os Painel de Controle itens que usam **CPlApplet** devem ser registrados de uma das duas maneiras:

-   Se o item Painel de Controle deve estar disponível para todos os usuários, registre o caminho por computador adicionando um valor **REG \_ EXPAND \_ SZ** à sub-chave **HKEY LOCAL \_ \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Painel de Controle** \\ **Cpls,** definida como o caminho DLL.
-   Se o Painel de Controle item estiver disponível por usuário, use **HKEY \_ CURRENT \_ USER** como a chave raiz em vez de **HKEY LOCAL \_ \_ MACHINE.**

Os dois exemplos a seguir registram o item de Painel de Controle *MyCplApp.* A DLL é chamada MyCpl.cpl e está localizada no diretório do aplicativo *\\ MyCorp MyApp.* Este primeiro exemplo ilustra o registro por computador.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Adicione essas informações ao Registro para registrar a existência do arquivo .cpl dados.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Etapa 2:

**Windows Vista e posterior:** Adicione essas informações adicionais ao Registro para fornecer um GUID para o Painel de Controle item.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

Ao gerar um GUID para identificar exclusivamente o item Painel de Controle, você pode adicionar links de tarefa ao Painel de Controle. Sem esse GUID, não há como os links de tarefa serem associados ao Painel de Controle item. Consulte [Criando links de tarefa pesquisáveis para um Painel de Controle item](creating-searchable-task-links.md).

### <a name="step-3"></a>Etapa 3:

**Windows Vista e posterior:** Adicione as informações a seguir ao Registro para criar um nome canônico para o item.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

Ao adicionar um nome canônico, os usuários podem iniciar o item Painel de Controle de uma linha de comando inserindo `control.exe /name MyCorporation.MyCpl` . Isso também possibilita alterar uma implementação de um arquivo .cpl para um arquivo .exe posteriormente, sem a necessidade de chamar programas para fazer alterações, pois eles podem continuar abrindo o item por meio de seu nome canônico. Para obter mais informações sobre nomes canônicos, [consulte Executando Painel de Controle Itens](executing-control-panel-items.md).

### <a name="step-4"></a>Etapa 4:

**Windows Vista e posterior:** Adicione as informações a seguir ao Registro para atribuir um Painel de Controle a uma ou mais categorias.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP:** Adicione as informações a seguir ao Registro para atribuir um Painel de Controle a uma ou mais categorias.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

Este exemplo atribui o item à categoria 3, que é Rede e Internet. Para adicionar um item a várias categorias, forneça a lista como um valor REG SZ separado por \_ vírgulas, como "3,8". Os valores podem ser fornecidos como decimal ou hexadecimal. Observe que a capacidade de adicionar um item a várias categorias só é possível Windows XP Service Pack 2 (SP2) e posterior. Consulte [Atribuindo Painel de Controle categorias para](assigning-control-panel-categories.md) todos os valores possíveis.

### <a name="step-5"></a>Etapa 5:

**Windows Vista e posterior:** Adicione as informações a seguir ao Registro para criar e apontar para um arquivo XML para manter links de tarefa para o item. O valor deve ser um caminho REG SZ, conforme mostrado aqui ou um módulo e uma ID de recurso \_ (por exemplo, "C: Arquivos de Programas \\ \\ MyCorp \\ MyAppMyApp.exe,-31") se for um recurso \\ inserido. O local do arquivo XML deve ser totalmente especificado. Ele não pode usar uma variável de ambiente, como %ProgramFiles%.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Para obter mais detalhes sobre links de tarefa e como criar o arquivo XML para mantê-los, consulte Criando [links de](creating-searchable-task-links.md)tarefa pesquisáveis para um Painel de Controle item .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando Painel de Controle itens](registering-control-panel-items.md)
</dt> <dt>

[Como registrar itens executáveis Painel de Controle executáveis](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
