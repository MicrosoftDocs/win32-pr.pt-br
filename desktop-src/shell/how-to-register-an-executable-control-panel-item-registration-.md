---
description: Para itens do painel de controle que são implementados como arquivos. exe, nenhuma exportação especial ou manipulação de mensagens é necessária. Qualquer arquivo. exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta do painel de controle.
title: Como registrar itens do painel de controle executável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011004"
---
# <a name="how-to-register-executable-control-panel-items"></a>Como registrar itens do painel de controle executável

Para itens do painel de controle que são implementados como arquivos. exe, nenhuma exportação especial ou manipulação de mensagens é necessária. Qualquer arquivo. exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta do painel de controle.

Um exemplo é usado aqui para demonstrar os requisitos de registro. O exemplo mostra como registrar um item do painel de controle chamado **minhas configurações** como um objeto de comando para que ele apareça na janela do painel de controle. A janela **minhas configurações** também aparece quando o comando `MyApp.exe /settings` é executado.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Gere um GUID para o item do painel de controle. O GUID identifica exclusivamente o item do painel de controle. Neste exemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` é o GUID do item do painel de controle.

### <a name="step-2"></a>Etapa 2:

Usando o GUID como um nome, adicione uma subchave ao registro da seguinte maneira.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

Os dados para a entrada padrão são simplesmente o \_ nome do reg sz do item do painel de controle. A entrada padrão pode ser útil para identificar a entrada GUID, mas é opcional.

### <a name="step-3"></a>Etapa 3:

Usando o GUID como um nome, adicione uma subchave e suas entradas ao registro da seguinte maneira.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Default**. REG \_ sz. O nome de exibição do item do painel de controle.
-   **Localizadastring**. Opcional. REG \_ sz ou reg \_ expande \_ sz. O nome do módulo e a ID da tabela de cadeia de caracteres do nome localizado do item do painel de controle. O formato é um sinal de "arroba" (@) seguido pelo nome do. exe ou. dll que contém a tabela de cadeia de caracteres MUI (Multilingual User interface). As variáveis de ambiente podem ser usadas como um substituto para uma parte do caminho. O caminho e o nome do arquivo são seguidos por uma vírgula (,) e um hífen (-), seguidos da ID na tabela de cadeias de caracteres.

    Se o módulo não tiver uma tabela de cadeia de caracteres, essa entrada poderá simplesmente ser a cadeia de caracteres do nome de exibição. Se você usar apenas a cadeia de caracteres de nome de exibição em vez de uma tabela de cadeia de caracteres, o nome não será ajustado para o idioma de exibição atual.

-   **InfoTip**. REG \_ sz ou reg \_ expande \_ sz. Uma descrição do item do painel de controle. Essas informações são mostradas em um InfoTip que é exibido quando o mouse passa sobre o ícone do item. A sintaxe é a mesma usada para a Localizadastring, incluindo a opção de simplesmente fornecer uma cadeia de caracteres em vez de uma referência de tabela de cadeia de caracteres.
-   **System. ApplicationName**. REG \_ sz. O nome canônico do item. O comando do formulário `control.exe /name System.ApplicationName` abre o item; por exemplo, `control.exe /name MyCorporation.MySettings` . Consulte [executando itens do painel de controle](executing-control-panel-items.md) para obter mais informações sobre o uso de Control.exe.
-   **System. ControlPanel. Category**. REG \_ sz. Um valor que declara as categorias do painel de controle em que o item é exibido. Várias categorias são separadas por vírgulas. No caso do exemplo acima, a entrada especifica que o item **minhas configurações** deve aparecer nas categorias **aparência e personalização** e **programas** . Consulte [atribuindo categorias do painel de controle](assigning-control-panel-categories.md) para possíveis valores de categoria.
-   **System. software. TasksFileUrl**. REG \_ sz ou reg \_ expande \_ sz. O caminho do arquivo XML que define os [links de tarefas](creating-searchable-task-links.md). Isso pode ser um caminho de arquivo direto, conforme mostrado no exemplo, ou um recurso inserido especificado como um nome de módulo e uma ID de recurso, como "% ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".

### <a name="step-4"></a>Etapa 4:

Na mesma subchave GUID, adicione a seguinte subchave ao registro para fornecer o caminho do arquivo que contém o ícone e a ID de recurso da imagem dentro desse arquivo.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Observe que, embora a sintaxe seja semelhante às entradas localizadas e InfoTip discutidas anteriormente, nenhum caractere ' @ ' é usado como um prefixo na entrada REG \_ sz ou reg \_ expande- \_ sz que especifica o caminho.

### <a name="step-5"></a>Etapa 5:

Adicione as seguintes informações ao registro para fornecer o comando que é chamado pelo sistema quando o usuário abre o painel de controle.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Como registrar itens do painel de controle da DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



