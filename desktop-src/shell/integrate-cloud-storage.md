---
description: Mostra como se registrar como um provedor raiz de sincronização e integrar um provedor de armazenamento em nuvem ao nível raiz do Painel de Navegação.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integrar um provedor de Armazenamento nuvem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458196"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integrar um provedor de Armazenamento nuvem

Quando você tem um provedor de armazenamento em nuvem, há algumas etapas que você deve seguir para fornecer uma experiência consistente e preferencial para o usuário. Essas duas coisas estão se registrando como um provedor raiz de sincronização e integrando seu aplicativo ao nível raiz do Painel de Navegação.

> [!IMPORTANT]
> A integração do provedor de armazenamento em nuvem só tem suporte a partir do Windows 10.

 

A primeira coisa é registrar como um provedor raiz de sincronização. Isso permite que o Windows Shell saiba sobre seu aplicativo e que seu aplicativo será responsável por sincronizar arquivos em sua raiz de sincronização. Isso também permitirá que outros aplicativos saibam que você está sincronizando esses arquivos para que eles possam responder adequadamente. Outros aplicativos podem usar [**StorageFile.Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) para obter o [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) [**e a ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) do seu aplicativo.

Para se registrar como um provedor raiz de sincronização, você precisará criar várias entradas do Registro. Antes de fornecer a lista de pares chave-valor, aqui estão alguns espaço reservados que você deve substituir por seus próprios dados de aplicativo.

-   *\[ ID do \] provedor de armazenamento:* o nome do seu provedor de armazenamento em nuvem. Esse nome deve ser consistente, independentemente da versão do seu aplicativo. Um exemplo disso é OneDrive.
-   *\[ Windows SID: \]* o sid Windows que identifica o usuário. Se o aplicativo for compatível com várias instalações para vários usuários em um único computador, essa parte será necessária.
-   *\[ ID \] da conta:* o identificador do provedor de serviços para a conta atual desse usuário. Alguns provedores exigem a capacidade de fornecer várias raízes de sincronização para um usuário. Um exemplo disso é uma conta pessoal e de trabalho. A *ID da conta* permite que você tenha várias contas registradas para um usuário. Se o provedor dá suporte a várias raízes de sincronização por usuário, essa parte é necessária.

Esses espaço reservados são combinados para formar a ID raiz de sincronização. Você deve colocar um **!** caractere entre cada um dos espaço reservados ao formar a ID raiz de sincronização. Aqui estão os pares chave-valor que precisam ser criados.

-   **HKLM \\ Software \\ Microsoft Windows ID \\ \\ \\ \\ \\**** do provedor de armazenamento SyncRootManager do CurrentVersion Explorer !_\[ \]_ _\[ Windows \] SID_*_!_* _\[ ID \] da_ conta *_\\ DisplayNameResource:_* aponta para o recurso em que o shell Windows ou outros aplicativos podem obter um nome amigável para sua raiz de sincronização.
-   **HKLM \\ Software \\ Microsoft Windows ID \\ \\ \\ \\ \\**** do provedor de armazenamento SyncRootManager do CurrentVersion Explorer !_\[ \]_ _\[ Windows \] SID_*_!_* _\[ Ícone de \] ID da_*_\\ ContaResource:_* aponta para o recurso em que o shell Windows ou outros aplicativos podem obter um ícone para sua raiz de sincronização.
-   **HKLM \\ Software \\ Microsoft Windows ID \\ \\ \\ \\ \\**** do provedor de armazenamento SyncRootManager do CurrentVersion Explorer !_\[ \]_ _\[ Windows \] SID_*_!_* _\[ ID \] da conta_*_\\ UserSyncRoots \\_* Windows _\[ SID: \]_ o local no disco em que a raiz de sincronização está localizada.

Além de registrar-se como um provedor raiz de sincronização, você também deseja que os usuários tenham acesso fácil aos dados que você fornece. O namespace Explorador de Arquivos é projetado para fornecer um método para esse acesso fácil. Criar uma extensão de namespace para seu provedor e incorporá-la à janela Explorador de Arquivos permitirá que os usuários interajam com o nível raiz de seus serviços, assim como estão acostumados com outros Explorador de Arquivos itens. Este tópico explica como estender o namespace Explorador de Arquivos para que seu provedor apareça no nível raiz no Painel de Navegação.

O Painel de Navegação da Explorador de Arquivos janela é a parte da janela exibida no lado esquerdo. Na imagem abaixo, você pode ver a estrutura de namespace para esse usuário. O nível raiz no Painel de Navegação inclui os objetos **para OneDrive**, **Este PC** e **Rede**. Seguir estas etapas adicionará sua extensão ao mesmo nível.

![painel de navegação](images/navigationpane.png)

Para adicionar sua extensão ao Painel de Navegação, você precisará ter o seguinte antes de editar o Registro:

-   Uma pasta do sistema de arquivos que contém os dados a exibir ao usuário.

-   Nome do serviço de nuvem que será exibido no Painel de Navegação. Esse também pode ser o nome da instância se o serviço dá suporte a várias contas.

-   Ícone de identificação para seu aplicativo.

-   Uma CLSID para seu aplicativo. Uma maneira de gerar uma CLSID para seu aplicativo é usar o Uuidgen.exe. Consulte [ClSID Key para](../com/clsid-key-hklm.md) obter mais informações sobre CLSID.

As etapas a seguir modificam o Registro para obter as informações necessárias no namespace Explorador de Arquivos dados. As etapas específicas fazem três coisas.

-   Crie chaves no Registro para o CLSID que inclui valores para o nome e o ícone da extensão, bem como outras informações que definem seu comportamento.

-   Configure sua extensão para ser integrada ao Painel de Navegação no local apropriado e com a visibilidade adequada.

-   Configure sua extensão para ter o comportamento esperado para um elemento no painel de navegação.

Essas instruções usam especificamente o **reg.exe,** no entanto, você pode usar qualquer ferramenta de edição do Registro de sua escolha. Você pode até mesmo integrar essas etapas em um instalador que atualiza o Registro programaticamente.

## <a name="instructions"></a>Instruções

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Etapa 1: Adicionar o CLSID e nomear sua extensão

Adicione o nome da extensão ao Registro em HKEY \_ CURRENT \_ USER. Você também adicionará o identificador exclusivo para essa extensão. É possível adicionar mais de uma extensão por usuário, mas nesse caso, você precisará de um nome e identificador exclusivos para cada extensão. Esse nome e identificador devem ser consistentes durante o restante dessas etapas. Neste exemplo, o nome é *MyCloudStorageApp.*

> [!IMPORTANT]
> O identificador fornecido (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) nessas etapas é usado apenas como um exemplo. Você precisará alterar isso para seu CLSID exclusivo.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d "MyCloudStorageApp" /f**

### <a name="step-2-set-the-image-for-your-icon"></a>Etapa 2: Definir a imagem para o ícone

Forneça o caminho para o ícone que deve ser exibido no Painel de Navegação. No exemplo abaixo, *1043* refere-se ao identificador de recurso para o ícone na DLL indicada.

> [!IMPORTANT]
> Você precisa atualizar o caminho da imagem. Ele deve apontar para um caminho genérico em que seu aplicativo instalou uma imagem.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon /ve /t REG \_ EXPAND \_ SZ /d %SystemRoot%% \\ system32 \\imageres.dll,-1043 /f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Etapa 3: Adicionar sua extensão ao Painel de Navegação e torná-la visível

Definir esse valor como 0x1 indica que a extensão deve ser fixada. Isso garantirá que ele seja mostrado aos usuários por padrão. A configuração padrão para um usuário é que somente itens fixados serão mostrados no Painel de Navegação. Um usuário pode alterar essa configuração clicando com o botão direito do mouse no Painel de Navegação e selecionando **Mostrar todas as pastas**. Se você não quiser fixar sua extensão, poderá definir esse valor como 0x0. Isso não removerá sua extensão, mas simplesmente impedirá que ela seja exibida ao usuário por padrão.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v System.IsPinnedToNameSpaceTree /t REG \_ DWORD /d 0x1 /f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Etapa 4: Definir o local da extensão no Painel de Navegação

Isso é essencial para garantir que o Painel de Navegação fornece uma experiência consistente para o usuário.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v SortOrderIndex /t REG \_ DWORD /d 0x42 /f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Etapa 5: forneça a dll que hospeda sua extensão.

Use o shell32.dll para emular pastas padrão do Windows. Só altere isso se você tiver um motivo específico para fazer isso e estiver familiarizado com extensões de namespace.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32 /ve /t REG \_ EXPAND \_ SZ /d %systemroot%% \\ system32 \\shell32.dll /f**

### <a name="step-6-define-the-instance-object"></a>Etapa 6: Definir o objeto de instância

Indique que sua extensão de namespace deve funcionar como outras estruturas de pasta de arquivos Explorador de Arquivos. Para obter mais informações sobre objetos de instância de shell, consulte [Criando extensões de shell com objetos de instância de shell](/previous-versions/ms997573(v=msdn.10)).

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instância /v CLSID /t REG \_ SZ /d {0E5AAE11-A475-4c5b-AB00-C66DE400274E} /f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Etapa 7: Fornecer os atributos do sistema de arquivos da pasta de destino

Isso é necessário para garantir que o Explorador de Arquivos fornece uma experiência consistente e esperada para os usuários. Esse comando define **FILE \_ ATTRIBUTE \_ DIRECTORY** e **FILE ATTRIBUTE \_ \_ READONLY**, ambos são [**Constantes de Atributo de Arquivo**](../fileio/file-attribute-constants.md).

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v Attributes /t REG \_ DWORD /d 0x11 /f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Etapa 8: Definir o caminho para a raiz da sincronização

De definir o caminho para a raiz de sincronização.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v TargetFolderPath /t REG \_ EXPAND \_ SZ /d %USERPROFILE%% \\ MyCloudStorageApp /f**

### <a name="step-9-set-appropriate-shell-flags"></a>Etapa 9: Definir sinalizadores de shell apropriados

Definir alguns sinalizadores necessários para fixar sua extensão de namespace na árvore Explorador de Arquivos dados.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v FolderValueFlags /t REG \_ DWORD /d 0x28 /f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Etapa 10: Definir os sinalizadores apropriados para controlar o comportamento do shell

Definir os sinalizadores [**SFGAO**](sfgao.md) apropriados. Os sinalizadores relevantes são SFGAO \_ CANCOPY, SFGAO \_ CANLINK, \_ \_ SFGAO STORAGE, SFGAO HASPROPSHEET, \_ SFGAO STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ FOLDER, SFGAO FILESYSTEM e \_ SFGAO \_ HASSUBFOLDER.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v Attributes /t REG \_ DWORD /d 0xF080004D /f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Etapa 11: registrar sua extensão na raiz do namespace

Configure a extensão do namespace para ser um filho da pasta da área de trabalho.

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d MyCloudStorageApp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Etapa 12: ocultar sua extensão da área de trabalho

É importante que sua extensão apareça somente no painel de navegação do explorador de arquivos. Uma extensão de namespace não funciona como um atalho normal. Portanto, você não deve usar esse método para criar um atalho de área de trabalho.

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/t REG \_ DWORD/d 0x1/f**

 

 
