---
description: Para Painel de Controle itens implementados como arquivos .exe, nenhuma exportação especial ou manipulação de mensagens é necessária. Qualquer .exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta Painel de Controle dados.
title: Como registrar itens executáveis Painel de Controle executáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81e52e18bd2cd1c48d5d260b08844784a5286dd2cd4d9d5ec782a86f624fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009426"
---
# <a name="how-to-register-executable-control-panel-items"></a>Como registrar itens executáveis Painel de Controle executáveis

Para Painel de Controle itens implementados como arquivos .exe, nenhuma exportação especial ou manipulação de mensagens é necessária. Qualquer .exe pode ser registrado como um objeto de comando para aparecer com um ponto de entrada na pasta Painel de Controle dados.

Um exemplo é usado aqui para demonstrar os requisitos de registro. O exemplo mostra como registrar um item Painel de Controle chamado **My Configurações** como um objeto de comando para que ele apareça na janela Painel de Controle. A **janela Meu Configurações** também aparece quando o comando é `MyApp.exe /settings` executado.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Gere um GUID para o Painel de Controle item. O GUID identifica exclusivamente o Painel de Controle item. Neste exemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` é o GUID do Painel de Controle item.

### <a name="step-2"></a>Etapa 2:

Usando o GUID como um nome, adicione uma sub-chave ao Registro da seguinte forma.

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

Os dados para a entrada Padrão são simplesmente o nome \_ REG SZ do Painel de Controle item. A entrada Padrão pode ser útil para identificar a entrada GUID, mas é opcional.

### <a name="step-3"></a>Etapa 3:

Usando o GUID como um nome, adicione uma sub-chave e suas entradas ao Registro da seguinte forma.

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

-   **Default**. REG \_ SZ. O nome de exibição do Painel de Controle item.
-   **LocalizedString**. Opcional. REG \_ SZ ou REG \_ EXPAND \_ SZ. O nome do módulo e a ID da tabela de cadeia de caracteres do nome localizado do Painel de Controle item. O formato é um sinal "at" (@) seguido pelo nome do .exe ou .dll que contém a tabela de cadeia de caracteres Interface de Usuário Multilíngue (MUI). As variáveis de ambiente podem ser usadas como um substituto para uma parte do caminho. O caminho e o nome do arquivo são seguidos por uma vírgula (,) e um hífen (-), seguidos pela ID na tabela de cadeia de caracteres.

    Se o módulo não tiver uma tabela de cadeia de caracteres, essa entrada poderá ser simplesmente a cadeia de caracteres de nome de exibição. Se você usar apenas a cadeia de caracteres de nome de exibição em vez de uma tabela de cadeia de caracteres, o nome não se ajustará ao idioma de exibição atual.

-   **InfoTip**. REG \_ SZ ou REG \_ EXPAND \_ SZ. Uma descrição do Painel de Controle item. Essas informações são mostradas em uma InfoTip exibida quando o mouse passar o mouse sobre o ícone do item. A sintaxe é a mesma usada para LocalizedString, incluindo a opção de simplesmente fornecer uma cadeia de caracteres em vez de uma referência de tabela de cadeia de caracteres.
-   **System.ApplicationName.** REG \_ SZ. O nome canônico do item. O comando de formulário `control.exe /name System.ApplicationName` abre o item; por exemplo, `control.exe /name MyCorporation.MySettings` . Consulte [Executando Painel de Controle itens para](executing-control-panel-items.md) obter mais informações sobre o uso de Control.exe.
-   **System.ControlPanel.Category.** REG \_ SZ. Um valor que declara as Painel de Controle em que o item aparece. Várias categorias são separadas por vírgulas. No caso do exemplo acima, a entrada especifica que o item **Meu** Configurações deve aparecer nas categorias Aparência e **Personalização** **e** Programas. Consulte [Atribuindo Painel de Controle categorias para](assigning-control-panel-categories.md) possíveis valores de categoria.
-   **System.Software.TasksFileUrl.** REG \_ SZ ou REG \_ EXPAND \_ SZ. O caminho do arquivo XML que define os [links de tarefa](creating-searchable-task-links.md). Esse pode ser um caminho de arquivo direto, conforme mostrado no exemplo, ou um recurso inserido especificado como um nome de módulo e uma ID de recurso, como "%ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".

### <a name="step-4"></a>Etapa 4:

Sob essa mesma sub-chave GUID, adicione a sub-chave a seguir ao Registro para fornecer o caminho do arquivo que contém o ícone e a ID do recurso da imagem dentro desse arquivo.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Observe que, embora a sintaxe seja semelhante às entradas LocalizedString e InfoTip discutidas anteriormente, nenhum caractere '@' é usado como um prefixo na entrada REG SZ ou REG EXPAND SZ que especifica o \_ \_ \_ caminho.

### <a name="step-5"></a>Etapa 5:

Adicione as informações a seguir ao Registro para fornecer o comando que é chamado pelo sistema quando o usuário abre o Painel de Controle.

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

[Registrando Painel de Controle itens](registering-control-panel-items.md)
</dt> <dt>

[Como registrar itens de Painel de Controle DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



