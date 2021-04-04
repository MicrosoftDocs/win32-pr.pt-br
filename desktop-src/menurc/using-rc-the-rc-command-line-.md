---
title: Usando o RC (a linha de comando do RC)
description: Para iniciar o RC, use o comando a seguir.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917231"
---
# <a name="using-rc-the-rc-command-line"></a>Usando o RC (a linha de comando do RC)

Para iniciar o RC, use o comando a seguir.

**RC** \[ *Opções* \] do *arquivo de script*

O parâmetro *script-File* especifica o nome do arquivo de definição de recurso que contém os nomes, os tipos, os nomes de arquivo e as descrições dos recursos a serem compilados.

O RC pode gerar arquivos de recursos separados para aplicativos que têm recursos diferentes de idioma e idioma. Os desenvolvedores podem usar um [arquivo de configuração de recurso](/windows/desktop/Intl/preparing-resources) ou definir opções de linha de comando para selecionar quais tipos de recursos e itens são recursos não localizáveis do arquivo de [idioma neutro (ln)](/windows/desktop/Intl/mui-resource-management) e quais são recursos localizáveis de arquivos MUI específicos do idioma. Para obter mais informações, consulte a [interface do usuário multilíngüe](/windows/desktop/Intl/multilingual-user-interface).

O parâmetro *Options* pode ser uma ou mais das opções de linha de comando a seguir.

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

Define um símbolo para o pré-processador que você pode testar com a diretiva [**\# ifdef**](-ifdef.md) .

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*
</dt> <dd>

RC cria um idioma neutro. Arquivo RES e um MUI (dependente de idioma). Arquivo RES usando *script-File*. Essa opção deve ser usada junto com a opção **/fo** *resname* . O RC nomeia o idioma-neutro. Arquivo RES *resname. res* e nomeia o MUI (dependente do idioma). Arquivo RES *mresname. res*.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC cria um. Arquivo RES chamado *resname* usando *script-File*.

Se a opção **/FM** *mresname* também for definida, RC criará um idioma neutro. Arquivo RES e um MUI (dependente de idioma). Arquivo RES.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/G1**
</dt> <dd>

Se/G1, for definido, RC gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão. Se/G1 não for definido, o RC não gerará um arquivo MUI se o único recurso localizável que está sendo incluído no arquivo MUI for um recurso de versão.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Exibe a lista de opções de linha de comando.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Pesquisa o diretório especificado antes de Pesquisar os diretórios especificados pela variável de ambiente INCLUDE.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

Os tipos de recursos localizáveis RC colocam no MUI (dependente do idioma). Arquivo RES. Se a opção **/q** também for definida, essa opção será ignorada e as informações no arquivo de configuração RC prevalecerão.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *sobrescrever*
</dt> <dd>

Sobreposição de tipos de recursos que o RC coloca em ambos os idiomas neutros. RES e o MUI (dependente de idioma). Arquivos RES. Os tipos de recurso que são especificados pela opção **/k** devem ser um subconjunto daqueles especificados pela opção **/j** . Por exemplo,? J2 ? J3 ? K3 especifica que o RC coloca o tipo de recurso 3 nos arquivos de idioma neutro e dependente de idioma (MUI). Se a opção **/q** também for definida, essa opção será ignorada e as informações no arquivo de configuração RC prevalecerão.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*
</dt> <dd>

Especifica o idioma padrão para compilação. Por exemplo,-l409 é equivalente a incluir a seguinte instrução na parte superior do arquivo de script de recurso: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Para obter mais informações, consulte [identificadores de idioma](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**opção**
</dt> <dd>

NULL encerra todas as cadeias de caracteres na tabela de cadeias.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *mui. RCConfig*
</dt> <dd>

Um arquivo de configuração RC que segue o formato de arquivo de configuração RC. O formato de arquivo de configuração RC permite que os componentes descrevam automaticamente as informações de recursos, como controle de versão de recursos, caminho do arquivo MUI, tipos de recursos e itens. Esse arquivo especifica quais recursos vão para o idioma neutro. Arquivo RES e quais recursos vão para o MUI (dependente de idioma). Arquivo RES. Essa opção e as informações fornecidas no arquivo de configuração RC substituem as opções de linha de comando **/j** e **/k**.

**Windows Server 2003 e Windows XP/2000:** Essa opção não está disponível sem usar também as funções [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) em um sistema atualizado.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignorado. Fornecido para compatibilidade com os makefiles existentes.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u**
</dt> <dd>

Desdefine um símbolo para o pré-processador.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Exibe mensagens que relatam o progresso do compilador.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

Impede que o RC Verifique a variável de ambiente INCLUDE ao procurar arquivos de cabeçalho ou arquivos de recursos.

</dd> </dl>

## <a name="remarks"></a>Comentários

As opções não diferenciam maiúsculas de minúsculas e um hífen (-) pode ser usado no lugar de uma barra (/). Você pode combinar opções de letra única se elas não exigirem parâmetros adicionais.

O RC não gerará um arquivo MUI nos casos a seguir.

-   Não existem recursos localizáveis no arquivo. rc.
-   A única ID de idioma do recurso especificada no arquivo. rc é neutra (0x0).
-   O arquivo. RC tem recursos que são especificados em mais de um idioma. A exceção é que se o arquivo. rc contiver dois idiomas, e um idioma for neutro (0x0), o RC gerará um arquivo MUI.

Para mais informações, consulte os seguintes tópicos:

-   [Definindo nomes para o pré-processador](defining-names-for-the-preprocessor.md)
-   [Renomeando o arquivo de recurso compilado](renaming-the-compiled-resource-file.md)
-   [Procurando arquivos](searching-for-files.md)
-   [Exibindo mensagens de progresso](displaying-progress-messages.md)
-   [Mensagens de diagnóstico RC](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface do Usuário Multilíngue](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 