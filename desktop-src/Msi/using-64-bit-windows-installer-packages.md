---
description: Siga as diretrizes a seguir ao criar um pacote de Windows Installer de 64 bits.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: Usando pacotes de Windows Installer de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751177"
---
# <a name="using-64-bit-windows-installer-packages"></a>Usando pacotes de Windows Installer de 64 bits

Ao criar [pacotes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) ou aplicativos que chamam Windows Installer para instalar pacotes de 64 bits, faça o seguinte:

-   Use um esquema de banco de dados Windows Installer de 200 ou superior. Especifique que a versão 2,0 é a versão mínima do instalador necessária para instalar o pacote, definindo a propriedade de [**Resumo contagem de páginas**](page-count-summary.md) como o inteiro 200. Versões anteriores do Windows Installer rejeitam tentativas de instalar pacotes de 64 bits. Para pacotes de 64 bits na plataforma Arm64, o esquema de banco de dados Windows Installer deve ser 500 ou superior.
-   Indique na propriedade [**Resumo do modelo**](template-summary.md) do fluxo de informações de resumo do pacote que este é um pacote de 64 bits. Digite "Intel64" no campo plataforma da propriedade **Resumo do modelo** se o pacote for para ser executado em um processador Intel64. Digite "x64" se o pacote for para ser executado em um processador estendido de 64 bits. Digite "Arm64" se o pacote for para ser executado em um processador Arm64. Um pacote não pode ser marcado como compatível com plataformas Intel64 e x64, um valor de propriedade de **Resumo de modelo** de "Intel64, x64" é inválido. Um pacote não pode ser marcado como compatível com plataformas de 32 bits e 64 bits, os valores de propriedade de **Resumo de modelo** "Intel, x64" ou "Intel, Intel64" são inválidos.
-   Identifique cada componente de 64 bits definindo o **msidbComponentAttributes64bit** na coluna atributos da tabela de [componentes](component-table.md) .
-   Use instruções condicionais opcionais que verifiquem a versão do sistema operacional de 64 bits referenciando a propriedade [**VersionNT64**](versionnt64.md) . Windows Installer define essa propriedade como a versão do Windows de 64 bits e deixa VersionNT64 indefinida se o sistema operacional não for um Windows de 64 bits. Para obter mais informações, consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).
-   Use instruções condicionais opcionais que verifiquem o nível numérico do processador do computador referenciando a propriedade [**Intel64**](intel64.md) ou [**Msix64**](msix64.md) . O Windows Installer define essas propriedades para o nível de processador numérico atual do computador e deixa a propriedade **Intel64** indefinida se não for um processador baseado em Itanium. Para obter mais informações, consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).
-   Use a [tabela AppSearch](appsearch-table.md) e a [ação AppSearch](appsearch-action.md) para fazer pesquisas opcionais do registro para componentes de 64 bits existentes. Para procurar componentes de 64 bits existentes, inclua o bit **msidbLocatorType64bit** na coluna Type da [tabela RegLocator](reglocator-table.md). Para obter mais informações, consulte [pesquisando aplicativos existentes, arquivos, entradas de registro ou propriedade de entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Obtenha os caminhos para as pastas do sistema referenciando a propriedade [**System64Folder**](system64folder.md), a propriedade [**ProgramFiles64Folder**](programfiles64folder.md) e a propriedade [**CommonFiles64Folder**](commonfiles64folder.md) para as pastas de 64 bits e a propriedade [**SystemFolder**](systemfolder.md) , a propriedade [**ProgramFilesFolder**](programfilesfolder.md) e a propriedade [**CommonFilesFolder**](commonfilesfolder.md) para as pastas de 32 bits.
-   Verifique se o aplicativo usa o GUID correto ao fazer referência a um componente de 64 bits. Se houver versões de 32 bits e 64 bits de um componente específico, elas deverão ter GUIDs de ID de componente diferentes.
-   Determine se as novas variáveis de ambiente precisam ser definidas durante a instalação de aplicativos de 64 bits.
-   Se um Gerenciador de driver ODBC de 64 bits for instalado, o componente que o transporta deve ser nomeado ODBCDriverManager64. O Gerenciador de driver ODBC deve ser criado no pacote do instalador e um componente chamado ODBCDriverManager64 deve ser incluído. O gerente será instalado, se necessário.
-   Verifique se o aplicativo chama apenas os serviços de 32 bits executados como executáveis. Os aplicativos não devem chamar serviços de 32 bits executados em DLLs.
-   Se o aplicativo instalar versões coexistentes de 32 bits e 64 bits de um componente, verifique se o aplicativo compartilha informações do arquivo. ini corretamente.
-   Verifique se o aplicativo aplica apenas patches de 32 bits a binários de 32 bits e patches de 64 bits para binários de 64 bits.
-   Considere os cenários de atualização futura para as versões de 32 bits e 64 bits e mantenha os códigos de atualização. Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).
-   Ao usar um aplicativo de [inicialização](bootstrapping.md) para instalar um [pacote de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), compile o aplicativo de inicialização como um aplicativo de 64 bits.
-   Para desabilitar a [reflexão do registro](../winprog64/registry-reflection.md) para chaves do registro que são afetadas por um determinado componente, defina o bit **MsidbComponentAttributesDisableRegistryReflection** no campo atributos da tabela de [componentes](component-table.md) . Pode ser necessário ter cópias de 32 bits e 64 bits do mesmo aplicativo coexistirem. Se esse bit for definido, o Windows Installer chamará a função [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) em cada chave que está sendo acessada pelo componente. Esse bit está disponível com Windows Installer versão 4,0. Esse bit é ignorado em sistemas de 32 bits. Esse bit é ignorado nas versões de 64 bits do Windows XP e do Windows 2000.

> [!Note]  
> O valor da raiz numérica do registro retornado pelo parâmetro *lpPathBuf* da função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue entre componentes em sistemas operacionais de 32 bits e 64 bits. Para obter mais informações, consulte função **MsiGetComponentPath** .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ações personalizadas de 64 bits](64-bit-custom-actions.md)
</dt> </dl>

 

 
