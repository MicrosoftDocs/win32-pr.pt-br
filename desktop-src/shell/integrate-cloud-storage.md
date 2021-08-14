---
description: Mostra como registrar-se como um provedor de raiz de sincronização e integrar um provedor de armazenamento em nuvem no nível raiz do painel de navegação.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: integrar um provedor de Armazenamento de nuvem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458196"
---
# <a name="integrate-a-cloud-storage-provider"></a>integrar um provedor de Armazenamento de nuvem

Quando você tem um provedor de armazenamento em nuvem, há algumas etapas que devem ser executadas para fornecer uma experiência consistente e preferencial para o usuário. Essas duas coisas estão se registrando como um provedor de raiz de sincronização e integrando seu aplicativo no nível raiz do painel de navegação.

> [!IMPORTANT]
> A integração do seu provedor de armazenamento em nuvem só tem suporte a partir do Windows 10.

 

A primeira coisa é registrar-se como um provedor de raiz de sincronização. isso permite que o Shell de Windows saiba sobre seu aplicativo e que seu aplicativo será responsável por sincronizar arquivos em sua raiz de sincronização. Isso também permitirá que outros aplicativos saibam que você está sincronizando esses arquivos para que eles possam responder adequadamente. Outros aplicativos podem usar [**StorageFile. Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) para obter o [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) e a [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) do seu aplicativo.

Para se registrar como um provedor de raiz de sincronização, você precisará criar várias entradas de registro. Antes de fornecer a lista de pares chave-valor, aqui estão alguns espaços reservados que você deve substituir por seus próprios dados de aplicativo.

-   *\[ ID \] do provedor de armazenamento*: o nome do seu provedor de armazenamento em nuvem. Esse nome deve ser consistente, independentemente da versão do seu aplicativo. Um exemplo disso é OneDrive.
-   *\[ sid \] de Windows*: o sid de Windows exclusivo que identifica o usuário. Se seu aplicativo der suporte a várias instalações para vários usuários em um único computador, essa parte será necessária.
-   *\[ ID \] da conta*: o identificador do provedor de serviços para a conta atual deste usuário. Alguns provedores exigem a capacidade de fornecer várias raízes de sincronização para um usuário. Um exemplo disso é um trabalho e uma conta pessoal. A *ID da conta* permite que você tenha várias contas registradas para um usuário. Se seu provedor der suporte a várias raízes de sincronização por usuário, essa parte será necessária.

Esses espaços reservados são combinados em conjunto para formar a ID raiz da sincronização. Você deve inserir um **!** caractere entre cada um dos espaços reservados ao formar a ID da raiz de sincronização. Aqui estão os pares chave-valor que precisam ser criados.

-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] da conta_*_\\ DisplayNameResource_* : aponta para o recurso em que o Shell de Windows ou outros aplicativos podem obter um nome amigável para a raiz de sincronização.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] da conta_*_\\ IconResource_* : aponta para o recurso em que o Shell de Windows ou outros aplicativos podem obter um ícone para a raiz de sincronização.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] da conta_*_\\ UserSyncRoots \\_*_\[ Windows \] SID_ : o local no disco onde a raiz de sincronização está localizada.

Além de registrar como um provedor de raiz de sincronização, você também deseja que os usuários tenham acesso fácil aos dados fornecidos. O namespace do explorador de arquivos foi projetado para fornecer um método para esse fácil acesso. Criar uma extensão de namespace para seu provedor e incorporá-la na janela Explorador de arquivos permitirá que os usuários interajam com o nível raiz de seus serviços, assim como são usados para outros itens do explorador de arquivos. Este tópico explica como estender o namespace do explorador de arquivos para que seu provedor seja exibido no nível raiz no painel de navegação.

O painel de navegação da janela Explorador de arquivos é a parte da janela exibida no lado esquerdo. Na imagem abaixo, você pode ver a estrutura de namespace para esse usuário. o nível raiz no painel de navegação inclui os objetos para **OneDrive**, **este computador** e a **rede**. Seguir essas etapas adicionará sua extensão ao mesmo nível.

![painel de navegação](images/navigationpane.png)

Para adicionar sua extensão ao painel de navegação, você precisará ter o seguinte antes de editar o registro:

-   Uma pasta do sistema de arquivos que contém os dados a serem exibidos para o usuário.

-   Nome do serviço de nuvem que será exibido no painel de navegação. Esse também pode ser o nome da instância se o seu serviço der suporte a várias contas.

-   Ícone identificável para seu aplicativo.

-   Um CLSID para seu aplicativo. Uma maneira de gerar um CLSID para seu aplicativo é usar o Uuidgen.exe. Consulte [chave de CLSID](../com/clsid-key-hklm.md) para obter mais informações sobre CLSID.

As etapas a seguir modificam o registro para obter as informações necessárias no namespace do explorador de arquivos. As etapas específicas fazem três coisas.

-   Crie chaves no registro para seu CLSID que inclua valores para o nome e o ícone de sua extensão, bem como outras informações que definem seu comportamento.

-   Configure sua extensão para ser integrada ao painel de navegação no local apropriado e com a visibilidade correta.

-   Configure sua extensão para ter o comportamento esperado para um elemento no painel de navegação.

Essas instruções usam especificamente o comando **reg.exe** , no entanto, você pode usar qualquer ferramenta de edição de registro de sua escolha. Você pode até mesmo integrar essas etapas em um instalador que atualiza o registro de forma programática.

## <a name="instructions"></a>Instruções

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Etapa 1: adicionar seu CLSID e nomear sua extensão

Adicione o nome de sua extensão ao registro em HKEY \_ Current \_ User. Você também adicionará o identificador exclusivo para essa extensão. É possível adicionar mais de uma extensão por usuário, mas nesse caso, você precisará de um nome e identificador exclusivos para cada extensão. Esse nome e identificador devem ser consistentes em todo o restante dessas etapas. Neste exemplo, o nome é *MyCloudStorageApp*.

> [!IMPORTANT]
> O identificador fornecido (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) nessas etapas é usado apenas como um exemplo. Você precisará alterar isso para seu CLSID exclusivo.

 

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t reg \_ sz/d "MyCloudStorageApp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>Etapa 2: definir a imagem para o ícone

Forneça o caminho para o ícone que deve ser exibido no painel de navegação. No exemplo a seguir, *1043* refere-se ao identificador de recurso para o ícone na DLL indicada.

> [!IMPORTANT]
> Você precisa atualizar o caminho da imagem. Ele deve apontar para um caminho genérico em que seu aplicativo instalou uma imagem.

 

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t reg \_ expande \_ /d%% SystemRoot%% \\ System32 \\imageres.dll,-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Etapa 3: adicionar sua extensão ao painel de navegação e torná-la visível

Definir esse valor como 0x1 indica que a extensão deve ser fixada. Isso garantirá que ele seja mostrado aos usuários por padrão. A configuração padrão para um usuário é que somente itens fixados serão mostrados no painel de navegação. Um usuário pode alterar essa configuração clicando com o botão direito do mouse no painel de navegação e selecionando **Mostrar todas as pastas**. Se você não quiser fixar sua extensão, poderá definir esse valor como 0x0. Isso não removerá sua extensão, mas simplesmente impedirá que ela seja exibida para o usuário por padrão.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/v System. IsPinnedToNameSpaceTree/t reg \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Etapa 4: definir o local para sua extensão no painel de navegação

Isso é essencial para garantir que o painel de navegação forneça uma experiência consistente para o usuário.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/V SortOrderIndex/t reg \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Etapa 5: fornecer a DLL que hospeda sua extensão.

Use o shell32.dll para emular pastas padrão do Windows. Altere isso apenas se você tiver um motivo específico para fazer isso e estiver familiarizado com extensões de namespace.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InprocServer32/ve/t reg \_ expande \_ /d%% systemroot%% \\ System32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>Etapa 6: definir o objeto de instância

Indique que a extensão do namespace deve funcionar como outras estruturas de pasta de arquivo no explorador de arquivos. Para obter mais informações sobre objetos de instância de Shell, consulte [criando extensões de shell com objetos de instância de shell](/previous-versions/ms997573(v=msdn.10)).

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instância/v CLSID/T reg \_ sz/d {0E5AAE11-A475-4c5b-AB00-C66DE400274E}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Etapa 7: fornecer os atributos do sistema de arquivos da pasta de destino

Isso é necessário para garantir que o explorador de arquivos forneça uma experiência consistente e esperada para os usuários. Esse comando define **o \_ \_ diretório de atributo de arquivo** e o atributo de **arquivo \_ \_ ReadOnly**, ambos os quais são [**constantes de atributo de arquivo**](../fileio/file-attribute-constants.md).

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instância \\ InitPropertyBag/v atributos/t reg \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Etapa 8: definir o caminho para a raiz de sincronização

Defina o caminho para a raiz de sincronização.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instância \\ InitPropertyBag/v TargetFolderPath/t reg \_ expandir \_ sz/d%% USERPROFILE%% \\ MyCloudStorageApp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>Etapa 9: definir sinalizadores de shell apropriados

Defina alguns sinalizadores necessários para fixar a extensão do namespace na árvore do explorador de arquivos.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ identificação ShellFolder/v FolderValueFlags/t reg \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Etapa 10: definir os sinalizadores apropriados para controlar o comportamento do Shell

Defina os sinalizadores [**SFGAO**](sfgao.md) apropriados. Os sinalizadores relevantes são SFGAO \_ cancopie, SFGAO \_ canlink, SFGAO \_ armazenamento, SFGAO \_ HASPROPSHEET, SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ Folder, SFGAO \_ FileSystem e SFGAO \_ HASSUBFOLDER.

**REG add HKCU \\ software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ identificação ShellFolder/v atributos/t reg \_ DWORD/d 0xF080004D/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Etapa 11: Registrar sua extensão na raiz do namespace

Configure a extensão de namespace para ser um filho da pasta da área de trabalho.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer Desktop \\ \\ \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d MyCloudStorageApp /f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Etapa 12: Ocultar sua extensão da Área de Trabalho

É importante que sua extensão apareça apenas no Painel de Navegação do Explorador de Arquivos. Uma extensão de namespace não funciona como um atalho normal. Portanto, você não deve usar esse método para criar um atalho da Área de Trabalho.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ HideDesktopIcons \\ NewStartPanel /v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /t REG \_ DWORD /d 0x1 /f**

 

 
