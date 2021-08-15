---
title: Usando o RC (a linha de comando do RC)
description: Para iniciar o RC, use o comando a seguir.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e560ebee4312dccc2463caf123f05a5ad9831cd293c9976350e6de7ee13cb64a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971915"
---
# <a name="using-rc-the-rc-command-line"></a>Usando o RC (a linha de comando do RC)

Para iniciar o RC, use o comando a seguir.

**RC** \[ *opções* \] *arquivo de script*

O *parâmetro script-file* especifica o nome do arquivo de definição de recurso que contém os nomes, tipos, nomes de arquivo e descrições dos recursos a serem compilados.

O RC pode gerar arquivos de recursos separados para aplicativos que têm recursos específicos de idioma e neutros. Os desenvolvedores [](/windows/desktop/Intl/preparing-resources) podem usar um arquivo de configuração de recursos ou definir opções de linha de comando para selecionar quais tipos de recursos e itens são recursos não localizáveis do arquivo [LN (neutral](/windows/desktop/Intl/mui-resource-management) de idioma) e quais são recursos localizáveis de arquivos de MUI específicos do idioma. Para obter mais informações, consulte o [Interface de Usuário Multilíngue](/windows/desktop/Intl/multilingual-user-interface).

O *parâmetro* options pode ser uma ou mais das opções de linha de comando a seguir.

## <a name="options"></a>Opções

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Exibe uma lista de opções de linha de comando.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

Define uma página de código usada pela conversão NLS.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Define um símbolo para o pré-processador que você pode testar com a [**\# diretiva ifdef.**](-ifdef.md)

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*
</dt> <dd>

O RC cria um com neutralidade de idioma. Arquivo RES e uma MUI (dependente de linguagem). Arquivo RES usando *o arquivo de script*. Essa opção deve ser usada junto com a **opção /fo** *resname.* RC nomeia o idioma neutro. O arquivo *RES resname.res e* nomeia a MUI (dependente de idioma). Arquivo RES *mresname.res*.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem também usar as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC cria um . Arquivo RES chamado *resname usando* *script-file*.

Se a **opção /fm** *mresname* também estiver definida, o RC criará um com neutralidade de idioma. Arquivo RES e uma MUI (dependente de linguagem). Arquivo RES.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem também usar as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/g1**
</dt> <dd>

Se /g1, estiver definido, RC gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão. Se /g1 não estiver definido, o RC não gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Exibe a lista de opções de linha de comando.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/i**
</dt> <dd>

Pesquisa o diretório especificado antes de pesquisar os diretórios especificados pela variável de ambiente INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

Os tipos de recursos localizáveis RC coloca na MUI (dependente de linguagem). Arquivo RES. Se a **opção /q** também estiver definida, essa opção será ignorada e as informações no arquivo de Configuração do RC têm precedência.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem também usar as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*
</dt> <dd>

Sobreposição de tipos de recursos que o RC coloca em ambas as linguagens neutras. RES e a MUI (dependente de idioma). Arquivos RES. Os tipos de recursos especificados pela **opção /k** devem ser um subconjunto daqueles especificados pela **opção /j.** Por exemplo, ? J2 ? J3 ? K3 especifica que o RC coloca o tipo de recurso 3 nos arquivos MUI (dependentes de idioma) e neutros em idioma. Se a **opção /q** também estiver definida, essa opção será ignorada e as informações no arquivo de Configuração do RC têm precedência.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem também usar as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

Especifica o idioma padrão para compilação. Por exemplo, -l409 é equivalente a incluir a seguinte instrução na parte superior do arquivo de script de recurso: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Para obter mais informações, consulte [Identificadores de idioma.](/windows/desktop/Intl/language-identifiers)

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Null encerra todas as cadeias de caracteres na tabela de cadeia de caracteres.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*
</dt> <dd>

Um arquivo de configuração RC que segue o formato do Arquivo de Configuração rc. O formato arquivo de configuração rc permite que os componentes descrevam informações de recursos como controle de versão de recursos, caminho do arquivo MUI, tipos de recursos e itens. Esse arquivo especifica quais recursos vão para o neutro no idioma. Arquivo RES e quais recursos vão para a MUI (dependente de linguagem). Arquivo RES. Essa opção e as informações fornecidas no arquivo de Configuração do RC substituem as opções de linha de comando **/j** e **/k**.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem também usar as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignorado. Fornecido para compatibilidade com makefiles existentes.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Indefini um símbolo para o pré-processador.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Exibe mensagens que relatam o progresso do compilador.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impede que o RC verifica a variável de ambiente INCLUDE ao pesquisar arquivos de header ou arquivos de recurso.

</dd> </dl>

## <a name="remarks"></a>Comentários

As opções não são sensíveis a minúsculas e um hífen (-) pode ser usado no lugar de uma barra (/). Você poderá combinar opções de letra única se elas não exigirem parâmetros adicionais.

O RC não gerará um arquivo MUI nos casos a seguir.

-   Não existem recursos localizáveis no arquivo .rc.
-   A única ID de linguagem de recurso especificada no arquivo .rc é neutra (0x0).
-   O arquivo .rc tem recursos especificados em mais de um idioma. A exceção será se o arquivo .rc contiver dois idiomas e um idioma for neutro (0x0), RC gerará um arquivo MUI.

Para obter mais informações, consulte estes tópicos:

-   [Definindo nomes para o pré-processador](defining-names-for-the-preprocessor.md)
-   [Renomeando o arquivo de recurso compilado](renaming-the-compiled-resource-file.md)
-   [Pesquisando arquivos](searching-for-files.md)
-   [Exibindo mensagens de progresso](displaying-progress-messages.md)
-   [Mensagens de diagnóstico rc](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface do Usuário Multilíngue](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 