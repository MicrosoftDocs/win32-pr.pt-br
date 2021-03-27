---
description: Os itens do painel de controle que são implementados em uma DLL que exporta a função CPlApplet têm requisitos de registro diferentes dos arquivos. exe.
title: Como registrar itens do painel de controle da DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662157"
---
# <a name="how-to-register-dll-control-panel-items"></a>Como registrar itens do painel de controle da DLL

> [!Note]  
> As diretrizes de implementação atuais estado que os novos itens do painel de controle devem ser implementados como arquivos. exe em vez de arquivos. cpl. As informações a seguir são incluídas principalmente para fins herdados.

 

Os itens do painel de controle que são implementados em uma DLL que exporta a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) têm requisitos de registro diferentes dos arquivos. exe. A partir do Windows XP, novas DLLs de item do painel de controle devem ser instaladas na pasta do aplicativo associado na pasta arquivos de programas. Os itens que são armazenados no diretório system32 com uma extensão. cpl não precisam ser registrados; Eles são mostrados automaticamente no painel de controle. Todos os outros itens do painel de controle que usam **CPlApplet** devem ser registrados de uma das duas maneiras:

-   Se o item do painel de controle estiver disponível para todos os usuários, registre o caminho por computador adicionando um valor **reg \_ expande \_ sz** à subchave **HKEY \_ \_ local** Computer \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** \\ **CPLs** , definida como o caminho da dll.
-   Se o item do painel de controle estiver disponível em uma base por usuário, use **HKEY \_ Current \_ User** como a chave raiz em vez de **HKEY \_ local \_ Machine**.

Os dois exemplos a seguir registram o item do painel de controle do *MyCplApp* . A DLL é denominada MyCpl.cpl e está localizada no diretório de aplicativo *MyCorp \\ MyApp* . Este primeiro exemplo ilustra o registro por computador.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Adicione essas informações ao registro para registrar a existência do arquivo. cpl.

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

**Windows Vista e posterior:** Adicione essas informações adicionais ao registro para fornecer um GUID para o item do painel de controle.

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

Ao gerar um GUID para identificar exclusivamente o item do painel de controle, você pode adicionar links de tarefas ao painel de controle. Sem esse GUID, não há nenhuma maneira de os links de tarefa serem associados ao item do painel de controle. Consulte [criando links de tarefas pesquisáveis para obter um item do painel de controle](creating-searchable-task-links.md).

### <a name="step-3"></a>Etapa 3:

**Windows Vista e posterior:** Adicione as seguintes informações ao registro para criar um nome canônico para o item.

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

Ao adicionar um nome canônico, os usuários podem iniciar o item do painel de controle em uma linha de comando digitando `control.exe /name MyCorporation.MyCpl` . Isso também torna possível alterar uma implementação de um arquivo. cpl para um arquivo. exe mais tarde, sem a necessidade de chamar programas para fazer alterações, já que eles podem continuar abrindo o item por meio de seu nome canônico. Para obter mais informações sobre nomes canônicos, consulte [executando itens do painel de controle](executing-control-panel-items.md).

### <a name="step-4"></a>Etapa 4:

**Windows Vista e posterior:** Adicione as seguintes informações ao registro para atribuir um item do painel de controle a uma ou mais categorias.

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

**Windows XP:** Adicione as seguintes informações ao registro para atribuir um item do painel de controle a uma ou mais categorias.

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

Este exemplo atribui o item à categoria 3, que é rede e Internet. Para adicionar um item a várias categorias, forneça a lista como um valor de sz de REG \_ separado por vírgulas, como "3, 8". Os valores podem ser fornecidos como Decimal ou hexadecimal. Observe que a capacidade de adicionar um item a várias categorias só é possível no Windows XP Service Pack 2 (SP2) e posterior. Consulte [atribuindo categorias do painel de controle](assigning-control-panel-categories.md) para todos os valores possíveis.

### <a name="step-5"></a>Etapa 5:

**Windows Vista e posterior:** Adicione as seguintes informações ao registro para criar e apontar para um arquivo XML para manter os links de tarefas para o item. O valor deve ser um \_ caminho reg sz, como mostrado aqui ou um módulo e uma ID de recurso (por exemplo, "C: \\ Program Files \\ mycorp \\ MyApp \\MyApp.exe,-31") se for um recurso incorporado. O local do arquivo XML deve ser totalmente especificado. Ele não pode usar uma variável de ambiente, como% ProgramFiles%.

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

Para obter mais detalhes sobre links de tarefas e como criar o arquivo XML para contê-los, consulte [criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Como registrar itens do painel de controle executável](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
