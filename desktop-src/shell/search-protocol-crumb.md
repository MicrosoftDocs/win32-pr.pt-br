---
description: Entenda como usar o argumento de trilha na interface do usuário do shell do Windows como um meio de controlar o escopo de uma pesquisa.
title: Argumento de trilha (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 543bc90647bbe1daed1a3a6d1f7bc54a4713a8ed
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403599"
---
# <a name="crumb-argument-the-windows-shell"></a>Argumento de trilha (o Shell do Windows)

O `crumb` argumento oferece suporte a instruções AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa. Além das instruções AQS, o `crumb` argumento pode usar um parâmetro especial `location` no Windows Vista e `kind` `store` parâmetros no Windows XP, conforme descrito posteriormente neste tópico.

Este tópico contém as seguintes seções:

-   [Sintaxe de trilha](#crumb-syntax)
    -   [Exemplos gerais](#general-examples)
-   [Usando a trilha com o Vista (local)](#using-crumb-with-vista-location)
    -   [Exemplos do vista](#vista-examples)
    -   [Constantes para pastas comuns](#constants-for-common-folders)
    -   [Informações do argumento](#argument-information)

## <a name="crumb-syntax"></a>Sintaxe de trilha

A sintaxe de trilha é a seguinte:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



A <column> parte é qualquer propriedade no sistema de propriedades e o <value> a parte é um valor válido para essa propriedade. A <label> parte é um alias opcional para a propriedade que é exibido como uma dica de interface do usuário.

### <a name="general-examples"></a>Exemplos gerais


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Usando a trilha com o Vista (local)

No parâmetro de trilha, o Windows Vista dá suporte ao AQS completo e também à `location` propriedade, que tem uma implementação especial disponível apenas no Windows Vista. Você pode usar uma cadeia de caracteres AQS ou a `location` propriedade dentro de um único parâmetro de trilha, mas não ambos. Se o parâmetro de trilha incluir AQS, todo o restante nesse parâmetro de trilha será ignorado.

A `location` propriedade permite que você especifique um caminho para pesquisar. O Windows Vista pode ignorar o indexador e atravessar o diretório diretamente se o local estiver fora do escopo de rastreamento do indexador. Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o indexador.

Quando você especifica uma `location` propriedade, dois parâmetros adicionais têm suporte e são opcionais:



| Parâmetro | Valores                  | Descrição                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusão | incluir, excluir        | Especifica se a consulta deve incluir ou excluir itens desse caminho. "Include" é o padrão. O Windows Vista não oferece suporte a exclusões sem inclusões. (Veja o exemplo) |
| recursão | recursivo, nonrecursive | Especifica se a pesquisa deve recurse todas as subpastas começando com o valor definido no local:<value>. "Recursivo" é o padrão.                             |



 

Para fazer o escopo de uma pesquisa usando o protocolo **Search:** , você tem opções diferentes, dependendo do destino do escopo.

Pasta em um computador local:

-   Use AQS (trilha = pasta: <caminho codificado de URL>)
-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

Pasta em um computador/rede remota:

-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

Pasta acessada por meio de um manipulador de protocolo UNC (Convenção de nomenclatura universal) conhecido:

-   Use AQS (trilha = armazenamento: <UNC protocol handler name> )
-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

### <a name="vista-examples"></a>Exemplos do vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



O primeiro exemplo executa uma pesquisa por "férias" começando no `shell://Personal` local (um atalho especial para a pasta **meus documentos** do usuário), incluindo essa pasta e todas as subpastas. Consulte a tabela abaixo.

O segundo exemplo executa uma pesquisa em C: \\ Pictures, mas não em c: \\ imagens \\ duplicatas.

O terceiro exemplo executa uma pesquisa em C: \\ Documents, limitada a arquivos com a `kind` propriedade definida como pics.

### <a name="constants-for-common-folders"></a>Constantes para pastas comuns

O Windows Vista permite o uso de valores CSIDl que fornecem uma maneira exclusiva independente do sistema de identificar pastas especiais usadas frequentemente por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema. Por exemplo, a pasta do sistema pode ser "C: \\ Windows" em um sistema e "c: \\ WinNT" em outro.

Use esses locais com esta sintaxe:


```
crumb=location:shell%3a<LocationName>&
```



A tabela a seguir lista os valores de CSIDl. Consulte [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para obter mais informações.



| Name                        | Pesquisar Cadeia de caracteres                   | Descrição                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FERRAMENTAS ADMINISTRATIVAS        | % 20TOOLS ADMINISTRATIVO          | Diretório do sistema de arquivos que serve como um repositório para ferramentas administrativas.                                                                                                            |
| APPDATA                     | APPDATA                         | Diretório do sistema de arquivos que serve como um repositório comum para dados específicos do aplicativo. Um caminho típico é C: \\ Documents and Settings \\ username \\ Application Data.                      |
| CACHE                       | CACHE                           | Diretório do sistema de arquivos que serve como um repositório comum para arquivos temporários da Internet. Um caminho típico é C: \\ Documents and Settings \\ nome de usuário \\ Temporary Internet Files.               |
| GRAVAÇÃO DE CD                  | CD% 20BURNING                    | Pasta que contém os dados a serem gravados no CD.                                                                                                                                             |
| FERRAMENTAS ADMINISTRATIVAS COMUNS | % 20ADMINISTRATIVE% 20TOOLS COMUM | Ferramentas administrativas para todos os usuários.                                                                                                                                                    |
| APPDATA COMUNS              | % 20APPDATA COMUM                | Dados de aplicativo para todos os usuários. Um caminho típico é C: \\ Documents and Settings \\ All Users \\ Application Data.                                                                             |
| ÁREA DE TRABALHO COMUM              | ÁREA DE TRABALHO COMUM                  | Dados do Microsoft Windows Desktop para todos os usuários. A pasta virtual que é a raiz do namespace.                                                                                        |
| DOCUMENTOS COMUNS            | % 20DOCUMENTS COMUM              | Documentos para todos os usuários. Um caminho típico é C: \\ Documents and Settings \\ All Users \\ My Documents.                                                                                        |
| PROGRAMAS COMUNS             | % 20PROGRAMS COMUM               | Grupos de programas comuns a todos os usuários. Um caminho típico é C: \\ Documents and Settings \\ todos os usuários \\ menu iniciar \\ programas.                                                                     |
| MENU INICIAR COMUM           | % 20START% 20MENU COMUM           | Itens do menu iniciar comuns a todos os usuários. Um caminho típico é o menu C: \\ Documents and Settings \\ All Users \\ Start.                                                                             |
| INICIALIZAÇÃO COMUM              | % 20STARTUP COMUM                | Grupo de programas de inicialização comum a todos os usuários.                                                                                                                                             |
| MODELOS COMUNS            | % 20TEMPLATES COMUM              | Modelos de documento comuns a todos os usuários.                                                                                                                                                |
| COMMONMUSIC                 | MEU% 20MUSIC                      | Meus modelos de pasta de música comuns a todos os usuários.                                                                                                                                         |
| COMMONPICTURES              | MEU% 20PICTURES                   | Modelos de pasta minhas imagens comuns a todos os usuários.                                                                                                                                      |
| COMMONVIDEO                 | MEU% 20VIDEO                      | Meus modelos de pasta de vídeo comuns a todos os usuários.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | pasta que contém dados de conexão.                                                                                                                                                     |
| PASTA DO PAINEL DE CONTROLE        | CONTROLPANELFOLDER              | Pasta virtual que contém ícones para os aplicativos do painel de controle.                                                                                                                    |
| ARAR                     | ARAR                         | Diretório do sistema de arquivos que serve como um repositório comum para cookies da Internet. Um caminho típico é C: \\ Documents and Settings \\ nome de usuário \\ cookies.                                        |
| DESKTOP                     | DESKTOP                         | Área de trabalho do Microsoft Windows. A pasta virtual que é a raiz do namespace.                                                                                                           |
| FAVORITOS                   | FAVORITOS                       | Diretório do sistema de arquivos que serve como um repositório comum para os itens favoritos do usuário. Um caminho típico é C: \\ Documents and Settings \\ username \\ Favorites.                             |
| TrueType                       | TrueType                           | Pasta virtual que contém as fontes instaladas. Um caminho típico é C: \\ Windows \\ fonts.                                                                                                       |
| HISTÓRICO                     | HISTÓRICO                         | Diretório do sistema de arquivos que serve como um repositório comum para itens de histórico da Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Pasta que contém dados da Internet.                                                                                                                                                    |
| APPDATA LOCAL               | % 20APPDATA LOCAL                 | Diretório do sistema de arquivos que serve como um repositório de dados para aplicativos locais (não móveis). Um caminho típico é C: \\ Documents and Settings \\ nome de usuário \\ configurações locais \\ dados de aplicativo. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Diretório de recursos localizado.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Meu Computador. Pasta virtual que contém tudo no computador local: dispositivos de armazenamento, impressoras e painel de controle. Essa pasta também pode conter unidades de rede mapeadas.             |
| MINHAS MÚSICAS                    | MEU% 20MUSIC                      | Minha pasta de música. Um caminho típico é C: \\ Documents and Settings \\ nome_de_usuário \\ My Documents \\ minha música.                                                                                       |
| MINHAS IMAGENS                 | MEU% 20PICTURES                   | Pasta minhas imagens. Um caminho típico é C: \\ Documents and Settings \\ nome_de_usuário \\ My Documents \\ minhas imagens.                                                                                 |
| MEU VÍDEO                    | MEU% 20VIDEO                      | Minha pasta de vídeo. Um caminho típico é C: \\ Documents and Settings \\ nome_de_usuário \\ My Documents \\ meu vídeo.                                                                                       |
| Netbastidores                     | Netbastidores                         | Pasta virtual que representa a raiz da hierarquia de namespace de rede.                                                                                                               |
| PASTA LOCAIS DE REDE       | NETWORKDPLACESFOLDER            | Uma pasta do sistema de arquivos que contém os objetos de link que podem existir na pasta virtual meus locais de rede. Não é o mesmo que o netbastidor, que representa a raiz do namespace de rede.   |
| LINKS DE OEM                   | % 20LINKS OEM                     | Pasta que contém links para sites OEM.                                                                                                                                                  |
| PESSOAL                    | PESSOAL                        | Diretório do sistema de arquivos que serve como um repositório comum para os documentos de um usuário. Um caminho típico é C: \\ Documents and Settings \\ nome_de_usuário \\ My Documents.                                 |
| PASTA IMPRESSORAS             | PASTA IMPRESSORAS                 | Pasta virtual que contém as impressoras instaladas.                                                                                                                                          |
| Diexaustos                   | Diexaustos                       | Diretório do sistema de arquivos que contém os objetos de link que podem existir na pasta virtual impressoras. Um caminho típico é C: \\ Documents and Settings \\ nome_de_usuário \\ outbastidores.                 |
| PROGRAMAS                    | PROGRAMAS                        | Diretório do sistema de arquivos que contém os grupos de programas do usuário (que também são diretórios do sistema de arquivos). Um caminho típico é C: \\ Documents and Settings \\ nome de usuário \\ menu iniciar \\ programas.  |
| PERFIL                     | PERFIL                         | Pasta de perfil do usuário.                                                                                                                                                                 |
| ARQUIVOS DE PROGRAMAS               | PROGRAMA% 20FILES                 | Pasta arquivos de programas. Um caminho típico é C: \\ Program Files.                                                                                                                             |
| ARQUIVOS DE PROGRAMAS COMUNS        | PROGRAMFILESCOMMON              | Pasta Arquivos de Programas comum a todos os usuários.                                                                                                                                              |
| ARQUIVOS DE PROGRAMAS COMUNS x86    | PROGRAMFILESCOMMONX86           | Pasta Arquivos de Programas comum a todos os usuários em máquinas x86.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Pasta Arquivos de Programas em máquinas x86.                                                                                                                                                  |
| Recente                      | Recente                          | Diretório do sistema de arquivos que contém os documentos usados mais recentemente pelo usuário. Um caminho típico é C: \\ Nome de usuário de Documentos e \\ Configurações \\ Recente.                                           |
| PASTA LIXEIRA          | RECYCLEBINFOLDER                | Pasta virtual que contém os objetos na conta do usuário Lixeira.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | O Diretório de recursos.                                                                                                                                                                |
| Sendto                      | Sendto                          | Diretório do sistema de arquivos que contém itens de menu Enviar para. Um caminho típico é C: Documentos e \\ Configurações nome \\ de usuário \\ SendTo.                                                                |
| MENU INICIAR                  | START%20MENU                    | Diretório do sistema de arquivos que contém menu Iniciar itens. Um caminho típico é C: Menu Iniciar nome de usuário documentos e \\ \\ \\ configurações.                                                                 |
| Inicialização                     | Inicialização                         | Diretório do sistema de arquivos que corresponde ao grupo de programas de inicialização do usuário.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Pasta do sistema em máquinas x86.                                                                                                                                                         |
| MODELOS                   | MODELOS                       | Diretório do sistema de arquivos que serve como um repositório comum para modelos de documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Pasta do sistema. Um caminho típico é C: \\ Sistema \\ Windows.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Diretório do Windows ou SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informações de argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



