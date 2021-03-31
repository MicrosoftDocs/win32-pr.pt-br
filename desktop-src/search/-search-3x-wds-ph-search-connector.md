---
description: O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do registro. Por meio do registro, tanto os implementadores quanto os terceiros podem permitir que os manipuladores de protocolo novos e herdados participem da pesquisa do Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Criando um conector de pesquisa para um manipulador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090095"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Criando um conector de pesquisa para um manipulador de protocolo

O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do registro. Por meio do registro, tanto os implementadores quanto os terceiros podem permitir que os manipuladores de protocolo novos e herdados participem da pesquisa do Windows 7.

Este tópico é organizado da seguinte maneira:

-   [Sobre os conectores de pesquisa para manipuladores de protocolo no Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Habilitando manipuladores de protocolo para participar da pesquisa](#enabling-protocol-handlers-to-participate-in-search)
    -   [Desabilitando a criação do conector de pesquisa de manipulador de protocolo](#disabling-protocol-handler-search-connector-creation)
    -   [Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Usando o redirecionamento de cadeia de caracteres do registro](#using-registry-string-redirection)
    -   [Restaurando um conector de pesquisa de manipulador de protocolo excluído](#restoring-a-deleted-protocol-handler-search-connector)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Sobre os conectores de pesquisa para manipuladores de protocolo no Windows 7

No Windows 7, as pesquisas no menu **Iniciar** ou no Windows Explorer incluem apenas arquivos em locais indexados e itens que não são do sistema de arquivos, como armazenamentos de dados remotos ou itens de manipulador de protocolo que têm um conector de pesquisa. Além de incluir os itens de manipulador de protocolo no escopo do menu **Iniciar** e das pesquisas do Shell, o conector de pesquisa habilita o menu **Iniciar** para agrupar itens de manipulador de protocolo nos resultados do menu **Iniciar** , com o benefício resultante de que o usuário pode clicar no cabeçalho do grupo e exibir os resultados somente do manipulador de protocolo. Como alternativa, o usuário pode navegar até a pasta **pesquisas** , abrir o arquivo do conector de pesquisa e executar uma pesquisa que inclui apenas itens do manipulador de protocolo específico associado a esse conector de pesquisa.

Quando um usuário inicia pela primeira vez um aplicativo que registra um manipulador de protocolo, o Windows Explorer gera um arquivo do conector de pesquisa (. searchConnector-MS) para o manipulador de protocolo na pasta **pesquisas** do usuário. Os aplicativos com manipuladores de protocolo podem optar por desabilitar esse comportamento ou personalizar o nome e a descrição do conector de pesquisa do manipulador de protocolo.

> [!Note]  
> O local da pasta de **pesquisas** do usuário é% USERPROFILE% de \\ pesquisas ou FolderId \_ SavedSearches. O GUID para FOLDERid \_ SavedSearches é {7d1d3a04-Debb-4115-95cf-2f29da2920da}.

 

O Windows Explorer controla a criação de um conector de pesquisa para um manipulador de protocolo por meio de entradas de chave do Registro descritas nas seções a seguir:

-   [Habilitando manipuladores de protocolo para participar da pesquisa](#enabling-protocol-handlers-to-participate-in-search)
-   [Desabilitando a criação do conector de pesquisa de manipulador de protocolo](#disabling-protocol-handler-search-connector-creation)
-   [Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Restaurando um conector de pesquisa de manipulador de protocolo excluído](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> Não há meios programáticos para criar um conector de pesquisa para um manipulador de protocolo. Eles devem ser configurados por meio do registro.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Habilitando manipuladores de protocolo para participar da pesquisa

As chaves do registro e seus valores possíveis são descritos na tabela a seguir. Um manipulador de protocolo pode popular algumas ou todas essas chaves do registro <protocol> , onde é substituído pelo nome real de seu protocolo, como MAPI, arquivo ou CSC, por exemplo.



| Chave do Registro                                                                                                                 | Valor (es) possível (is)                                                                                                                     | Type       | Comentários                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ versão                     | Não existe (padrão). Caso contrário, será 1 ou maior.                                                                               | REG \_ DWORD | Esse valor é usado para detectar alterações nos registros de modelo de localização para raízes de pesquisa que já foram processadas. Se não existir, use 0 como padrão. Como alternativa, aumente a versão para informar ao Windows Explorer que o conector de pesquisa deve ser regenerado porque uma versão mais recente do manipulador de protocolo foi instalada. |
| HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors | Não existe (padrão). Caso contrário, defina como 1.                                                                                         | REG \_ DWORD | Se não existir, crie um arquivo. searchconnector-MS na pasta pesquisas. Se 1, marque como processado e não faça nada.                                                                                                                                                                                                                                   |
| HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ Descrição padrão        | Uma cadeia de caracteres localizável que contém a descrição do conector de pesquisa.                                                              | REG \_ sz    | Opcional. Ele é usado no elemento Description do arquivo. searchconnector-MS.                                                                                                                                                                                                                                                                          |
| HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ \\ nome padrão               | Uma cadeia de caracteres localizada para nomear o conector de pesquisa. Usado como o nome do arquivo. searchconnector-MS.                                    | REG \_ sz    | Cada local deve ter um nome exclusivo. Na ausência desse valor, o nome de exibição fornecido pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do manipulador de protocolo será usado.                                                                                                                             |
| HKey \_ local \_ Machine \\ software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ padrão \\ FolderType         | Um GUID que identifica o [FOLDERTYPEID](../shell/foldertypeid.md) a ser aplicado ao conector de pesquisa. | REG \_ sz    | Opcional. Usado no elemento FolderType do arquivo. searchconnector-MS para indicar quais modelos devem ser usados para exibir os resultados. Por exemplo, o valor de GUID de \_ documentos FOLDERTYPEID.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Desabilitando a criação do conector de pesquisa de manipulador de protocolo

Se seu aplicativo expõe itens por meio de um manipulador de protocolo para uso no próprio aplicativo e você não deseja expor os itens por meio do Shell (no menu **Iniciar** e pesquisas do Windows Explorer), você precisa desabilitar a criação de um conector de pesquisa para o manipulador de protocolo.

Para desabilitar a criação do conector de pesquisa, defina DoNotCreateSearchConnectors como 0x00000001 (1), conforme mostrado no exemplo de chave do registro a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Se DoNotCreateSearchConnectors for definido como 1, recomendamos que você exponha a propriedade [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) em cada item exposto pelo manipulador de protocolo e defina o valor dessa propriedade como **true**. Isso impedirá que os itens do manipulador de protocolo apareçam no grupo de **arquivos** do menu **Iniciar** .

Se DoNotCreateSearchConnectors estiver presente e definido como zero, o Windows Explorer criará um conector de pesquisa para o manipulador de protocolo e os itens do manipulador de protocolo serão retornados no menu **Iniciar** e nas pesquisas do Windows Explorer.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Personalizando o nome, a descrição ou o FolderType para um conector de pesquisa de manipulador de protocolo

O nome do conector de pesquisa é usado não apenas para identificar o conector de pesquisa na pasta **pesquisas** , mas como o cabeçalho do grupo para os resultados em pesquisas do menu **Iniciar** . Portanto, é importante fornecer um nome descritivo para o conector de pesquisa. Se um nome não for fornecido na chave do registro, por padrão, o Windows Explorer usará o nome fornecido pela [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para a raiz de pesquisa do manipulador de protocolo e a descrição em branco. Você pode substituir o nome padrão por meio de uma entrada de chave do registro sem precisar renomear a interface IShellFolder. Embora não seja tão visível quanto o nome do conector de pesquisa, você também pode substituir a descrição do conector de pesquisa, fornecendo sua própria descrição.

Para substituir o nome ou a descrição padrão, defina as entradas conforme mostrado no exemplo de registro a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

Além disso, a entrada FolderType pode ser definida como um dos GUIDs [FOLDERTYPEID](../shell/foldertypeid.md) . O valor deve ser o GUID real e não seu nome. Por exemplo, {94d6ddcc-4a68-4175-A374-bd584a510b78} em vez de FOLDERTYPEID \_ Music. O GUID de um FOLDERTYPEID pode ser obtido no arquivo de cabeçalho Shlguid. h na [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>Usando o redirecionamento de cadeia de caracteres do registro

Você pode usar uma [cadeia de caracteres redirecionada](../intl/using-registry-string-redirection.md) para garantir que o nome fornecido para o conector de pesquisa possa ser localizado. Você pode incluir cadeias de caracteres localizáveis para as chaves de registro Name e Description em vez de inserir a cadeia de caracteres real no registro.

Para incluir uma cadeia de caracteres localizável para os valores de nome ou descrição, defina o valor conforme mostrado no exemplo de chave do registro a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

A cadeia de caracteres localizável usa o seguinte formato:

-   @dllname.dll,-ResourceId, em que:
    -   @dllname.dll é o caminho para a DLL que contém o recurso de cadeia de caracteres
    -   ResourceId é a ID de recurso de inteiro do recurso de cadeia de caracteres

O formato de uma cadeia de caracteres indireta, e uma cadeia de caracteres indireta anexada a um modificador de versão, é descrito na [função SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Restaurando um conector de pesquisa de manipulador de protocolo excluído

Como os conectores de pesquisa são arquivos no computador do usuário, eles podem ser excluídos por engano. Para restaurar todos os conectores de pesquisa de manipulador de protocolo excluídos, restaure as bibliotecas padrão. Para tanto, abra o Windows Explorer, clique com o botão direito do mouse na pasta **bibliotecas** e selecione **restaurar bibliotecas padrão**.

![captura de tela mostrando a opção de menu restaurar bibliotecas padrão](images/libraries.png)

## <a name="additional-resources"></a>Recursos adicionais

-   [IShellItem:: GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Noções básicas sobre manipuladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificando o índice das alterações](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Adicionando ícones e menus de contexto](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemplo de código: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Depuração de manipuladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
