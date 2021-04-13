---
description: Se um patch pode ser desinstalado depende de como o patch foi criado, a versão do Windows Installer usada para instalar o patch e as alterações feitas pelo patch para o aplicativo.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Patches desinstaláveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501267"
---
# <a name="uninstallable-patches"></a>Patches desinstaláveis

Se um patch pode ser desinstalado depende de como o patch foi criado, a versão do Windows Installer usada para instalar o patch e as alterações feitas pelo patch para o aplicativo. Se um patch não for desinstalado, a única maneira de remover o patch será desinstalar todo o aplicativo e reinstalá-lo sem aplicar o patch que está sendo removido.

Você pode chamar a desinstalação de patches aplicados com Windows Installer versão 3,0 usando opções de [linha de comando](command-line-options.md), a função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) ou o [**método RemovePatches**](installer-removepatches.md) , conforme descrito na seção [desinstalando patches](uninstalling-patches.md) . A Windows Installer verifica se cada um dos patches listados para remoção na propriedade [**MSIPATCHREMOVE**](msipatchremove.md) é desinstalável. Se o usuário não tiver privilégios para remover o patch, o patch é desconhecido para o produto, a política de patch impede a remoção ou o patch foi marcado como não desinstalado, o instalador retorna um erro indicando uma falha na transação de instalação.

**Windows Installer 2,0:** Sem suporte. Os patches aplicados usando uma versão do Windows Installer que é anterior ao Windows Installer 3,0 não são desinstaláveis.

## <a name="patches-that-are-not-uninstallable"></a>Patches que não são desinstaláveis

Um patch (arquivo. msp) aplicado a um aplicativo instalado não é desinstalável nos casos a seguir. O único método para remover um patch que não é desinstalável é desinstalar o aplicativo com patch e, em seguida, reinstalar o aplicativo sem reaplicar o patch. Nesse caso, você deve reaplicar os patches que você não deseja remover do aplicativo.

-   Os patches aplicados usando uma versão do Windows Installer com menos de Windows Installer 3,0 não são desinstaláveis.
-   Os patches aplicados aos aplicativos instalados em um computador que tenha a política [DisablePatchUninstall](disablepatchuninstall.md) definida por um administrador não são desinstaláveis. Quando essa [política de máquina](machine-policies.md)tiver sido definida, nenhum patch no computador poderá ser desinstalado, mesmo por um administrador.
-   Os patches que não têm uma tabela [MsiPatchMetaData](msipatchmetadata-table.md) em seu banco de dados não são desinstaláveis.
-   Os patches que não incluem a linha a seguir em sua tabela [MsiPatchMetaData](msipatchmetadata-table.md) não são desinstaláveis. O patch não é desinstalado para outros valores de empresa, propriedade e valor.

    | Empresa | Propriedade     | Valor |
    |---------|--------------|-------|
    | Nulo  | AllowRemoval | 1     |

    

     

-   O patch foi aplicado a um aplicativo instalado em um contexto para o qual o usuário tem privilégios insuficientes para desinstalar patches. As palavras "não permitidas" na tabela a seguir indicam que um usuário administrador ou não administrador não pode desinstalar patches de aplicativos com patch instalados neste contexto. A palavra "Allowed" nesta tabela significa que os privilégios não impedem que um administrador ou usuário não administrador desinstalem patches, no entanto, para qualquer um dos outros motivos discutidos nesta seção, ainda pode não ser possível desinstalar o patch.

    | Contexto de instalação do aplicativo        | Desinstalação do patch do administrador | Desinstalação de patch não administrador                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Permitido                          | Geralmente não permitido a única exceção é se o patch foi aplicado usando a aplicação de patch (LUA). Um patch marcado como um patch de LUA é desinstalado por administradores ou não administradores. A aplicação de patches de LUA só está disponível para pacotes instalados por máquina da mídia e exigem criação especial.<br/> |
    | Per-User não gerenciado para o usuário atual   | Permitido                          | Permitido                                                                                                                                                                                                                                                                                                          |
    | Per-User não gerenciado para um usuário diferente | Não Permitido                      | Não Permitido                                                                                                                                                                                                                                                                                                      |
    | Per-User gerenciado para o usuário atual       | Permitido                          | Não Permitido                                                                                                                                                                                                                                                                                                      |
    | Per-User gerenciado para um usuário diferente     | Não Permitido                      | Não Permitido                                                                                                                                                                                                                                                                                                      |

    

     

-   Uma [atualização importante](major-upgrades.md) aplicada por um patch não é desinstalável. As principais atualizações de um aplicativo devem ser executadas instalando o aplicativo atualizado (arquivo. msi) em vez de um patch.
-   Os patches aplicados a uma instalação administrativa não são desinstalados. A aplicação de patch de instalações administrativas não é recomendada. O conjunto atual de patches deve ser aplicado no computador do usuário depois que o usuário instalar o aplicativo a partir da imagem administrativa. Isso pode impedir que o [código do pacote](package-codes.md) em cache no computador do usuário se torne diferente do código do pacote na instalação administrativa. Se o código do pacote armazenado em cache no computador do usuário se tornar diferente daquele na instalação administrativa, reinstale o aplicativo da instalação administrativa e, em seguida, corrija o computador cliente.
-   Quando um patch adiciona novo conteúdo a qualquer uma das tabelas na lista a seguir, Windows Installer marca o patch como não desinstalável. Um patch desinstalável pode adicionar novos arquivos, assemblies, entradas de registro, componentes ou recursos a uma instalação do adicionando novas linhas a tabelas de banco de dados que não estão incluídas nesta lista.

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Classe](class-table.md)
    -   [ComPlus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [Duplicatafile](duplicatefile-table.md)
    -   [Ambiente](environment-table.md)
    -   [Extensão](extension-table.md)
    -   [Fonte](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [MIME](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCattribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [ProgId](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [Instalar o](serviceinstall-table.md)
    -   [Importação](typelib-table.md)
    -   [Verbo](verb-table.md)
    -   [!Note]  
        > Se um patch adicionar novo conteúdo às tabelas [RemoveFile](removefile-table.md) ou [RemoveRegistry](removeregistry-table.md) , Windows Installer não marcará o patch como não sendo desinstalável. No entanto, o patch não é desinstalado, a menos que o recurso para remover o novo conteúdo ainda não exista no pacote de instalação original. Por exemplo, se o patch adicionar uma nova linha à tabela removerfile, o arquivo removido não poderá ser restaurado desinstalando o patch se o arquivo for externo à [tabela de arquivos](file-table.md). O arquivo deve ter sido criado na tabela de arquivos do pacote original mais os patches aplicados para que o patch seja desinstalável.

         

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequenciamento de patch](sequencing-patches.md)
</dt> <dt>

[Removendo patches](removing-patches.md)
</dt> <dt>

[Desinstalando patches](uninstalling-patches.md)
</dt> <dt>

[Corrigir ações personalizadas de desinstalação de patch](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




