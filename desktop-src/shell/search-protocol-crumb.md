---
description: entenda como usar o argumento de trilha na interface do usuário do Windows Shell como um meio de controlar o escopo de uma pesquisa.
title: argumento de trilha (o Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3309f18cbd5a7e2769b264e516b019d9f3ed3b06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885432"
---
# <a name="crumb-argument-the-windows-shell"></a>argumento de trilha (o Shell de Windows)

O `crumb` argumento oferece suporte a instruções AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa. além das instruções AQS, o `crumb` argumento pode usar um parâmetro especial `location` no Windows Vista e `kind` `store` parâmetros no Windows XP, conforme descrito posteriormente neste tópico.

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



A &lt; parte da coluna &gt; é qualquer propriedade no sistema de propriedades e a &lt; parte do valor &gt; é um valor válido para essa propriedade. A <label> parte é um alias opcional para a propriedade que é exibido como uma dica de interface do usuário.

### <a name="general-examples"></a>Exemplos gerais


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Usando a trilha com o Vista (local)

no parâmetro de trilha, o Windows Vista dá suporte ao AQS completo e também à `location` propriedade, que tem uma implementação especial disponível apenas no Windows Vista. Você pode usar uma cadeia de caracteres AQS ou a `location` propriedade dentro de um único parâmetro de trilha, mas não ambos. Se o parâmetro de trilha incluir AQS, todo o restante nesse parâmetro de trilha será ignorado.

A `location` propriedade permite que você especifique um caminho para pesquisar. Windows O vista pode ignorar o indexador e atravessar o diretório diretamente se o local estiver fora do escopo de rastreamento do indexador. Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o indexador.

Quando você especifica uma `location` propriedade, dois parâmetros adicionais têm suporte e são opcionais:



| Parâmetro | Valores                  | Descrição                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusão | incluir, excluir        | Especifica se a consulta deve incluir ou excluir itens desse caminho. "Include" é o padrão. Windows O vista não oferece suporte a exclusões sem inclusões. (Veja o exemplo) |
| recursão | recursivo, nonrecursive | Especifica se a pesquisa deve recurse todas as subpastas a partir do valor definido no valor Location &lt; : &gt; . "Recursivo" é o padrão.                             |



 

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

Windows O Vista permite o uso de valores de CSIDl que fornecem uma maneira exclusiva independente do sistema de identificar pastas especiais usadas frequentemente por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema. por exemplo, a pasta do sistema pode ser "c: \\ Windows" em um sistema e "c: \\ Winnt" em outro.

Use esses locais com esta sintaxe:


```
crumb=location:shell%3a<LocationName>&
```



A tabela a seguir lista os valores de CSIDl. Consulte [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para obter mais informações.



| Nome                        | Pesquisar Cadeia de caracteres                   | Description                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FERRAMENTAS ADMINISTRATIVAS        | % 20TOOLS ADMINISTRATIVO          | Diretório do sistema de arquivos que serve como um repositório para ferramentas administrativas.                                                                                                            |
| APPDATA                     | APPDATA                         | Diretório do sistema de arquivos que serve como um repositório comum para dados específicos do aplicativo. um caminho típico é C: \\ documents e Configurações \\ nome de usuário de dados do \\ aplicativo.                      |
| CACHE                       | CACHE                           | Diretório do sistema de arquivos que serve como um repositório comum para arquivos temporários da Internet. um caminho típico é C: \\ documents e Configurações \\ nome de usuário \\ Temporary Internet files.               |
| GRAVAÇÃO DE CD                  | CD% 20BURNING                    | Pasta que contém os dados a serem gravados no CD.                                                                                                                                             |
| FERRAMENTAS ADMINISTRATIVAS COMUNS | % 20ADMINISTRATIVE% 20TOOLS COMUM | Ferramentas administrativas para todos os usuários.                                                                                                                                                    |
| APPDATA COMUNS              | % 20APPDATA COMUM                | Dados de aplicativo para todos os usuários. um caminho típico é C: \\ documents e Configurações \\ dados de aplicativos de todos os usuários \\ .                                                                             |
| ÁREA DE TRABALHO COMUM              | ÁREA DE TRABALHO COMUM                  | dados do Microsoft Windows Desktop para todos os usuários. A pasta virtual que é a raiz do namespace.                                                                                        |
| DOCUMENTOS COMUNS            | % 20DOCUMENTS COMUM              | Documentos para todos os usuários. um caminho típico é C: \\ documents e Configurações \\ todos os usuários \\ meus documentos.                                                                                        |
| PROGRAMAS COMUNS             | % 20PROGRAMS COMUM               | Grupos de programas comuns a todos os usuários. um caminho típico é C: \\ documents e Configurações \\ os \\ programas de Menu iniciar de todos os usuários \\ .                                                                     |
| MENU INICIAR COMUM           | % 20START% 20MENU COMUM           | menu Iniciar itens comuns a todos os usuários. um caminho típico é C: \\ documents e Configurações \\ Menu iniciar de todos os usuários \\ .                                                                             |
| INICIALIZAÇÃO COMUM              | % 20STARTUP COMUM                | Grupo de programas de inicialização comum a todos os usuários.                                                                                                                                             |
| MODELOS COMUNS            | COMMON%20TEMPLATES              | Modelos de documento comuns a todos os usuários.                                                                                                                                                |
| COMMONMUSIC                 | MY%20MUSIC                      | Modelos de pasta My Music comuns a todos os usuários.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | Modelos de pasta Minhas Imagens comuns a todos os usuários.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Modelos de pasta Meu Vídeo comuns a todos os usuários.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | pasta que contém dados de conexão.                                                                                                                                                     |
| PASTA PAINEL DE CONTROLE        | CONTROLPANELFOLDER              | Pasta virtual que contém ícones para os Painel de Controle aplicativos.                                                                                                                    |
| COOKIES                     | COOKIES                         | Diretório do sistema de arquivos que serve como um repositório comum para cookies da Internet. Um caminho típico é C: documentos e Configurações \\ cookies de nome de \\ \\ usuário.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Pasta virtual que é a raiz do namespace.                                                                                                           |
| FAVORITOS                   | FAVORITOS                       | Diretório do sistema de arquivos que serve como um repositório comum para os itens favoritos do usuário. Um caminho típico é C: Documentos \\ e Configurações \\ \\ favoritos de nome de usuário.                             |
| FONTES                       | FONTES                           | Pasta virtual que contém fontes instaladas. Um caminho típico é C: \\ \\ Fontes do WINDOWS.                                                                                                       |
| HISTÓRICO                     | HISTÓRICO                         | Diretório do sistema de arquivos que serve como um repositório comum para itens de histórico da Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Pasta que contém dados da Internet.                                                                                                                                                    |
| LOCAL APPDATA               | LOCAL%20APPDATA                 | Diretório do sistema de arquivos que serve como um repositório de dados para aplicativos locais (não móveis). Um caminho típico é C: documentos e Configurações nome de \\ usuário Local Configurações Dados do \\ \\ \\ Aplicativo. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Diretório de recursos localizado.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Meu Computador. Pasta virtual que contém tudo no computador local: dispositivos de armazenamento, impressoras e Painel de Controle. Essa pasta também pode conter unidades de rede mapeadas.             |
| MY MUSIC                    | MY%20MUSIC                      | Minha pasta Música. Um caminho típico é C: \\ Documentos e Configurações nome de usuário Meus Documentos Minha \\ \\ \\ Música.                                                                                       |
| MINHAS IMAGENS                 | MY%20PICTURES                   | Minha pasta Imagens. Um caminho típico é C: \\ Documentos e Configurações nome de usuário Meus Documentos Minhas \\ \\ \\ Imagens.                                                                                 |
| MEU VÍDEO                    | MY%20VIDEO                      | Minha pasta Vídeo. Um caminho típico é C: \\ Documentos e Configurações nome de usuário Meus Documentos Meu \\ \\ \\ Vídeo.                                                                                       |
| NET, NET, NET,                     | NET, NET, NET,                         | Pasta virtual que representa a raiz da hierarquia de namespace de rede.                                                                                                               |
| PASTA LOCAIS DE REDE       | NETWORKDPLACESFOLDER            | Uma pasta do sistema de arquivos que contém os objetos de link que podem existir na pasta virtual Meus Locais de Rede. Ele não é o mesmo que NET FIM, que representa a raiz do namespace de rede.   |
| OEM LINKS                   | OEM%20LINKS                     | Pasta que contém links para sites OEM.                                                                                                                                                  |
| PESSOAL                    | PESSOAL                        | Diretório do sistema de arquivos que serve como um repositório comum para documentos de um usuário. Um caminho típico é C: documentos \\ e Configurações nome de usuário \\ \\ Meus Documentos.                                 |
| PASTA IMPRESSORAS             | PASTA IMPRESSORAS                 | Pasta virtual que contém impressoras instaladas.                                                                                                                                          |
| PRINT PRINT SÃO                   | PRINT PRINT SÃO                       | Diretório do sistema de arquivos que contém os objetos de link que podem existir na pasta virtual Impressoras. Um caminho típico é C: \\ Documentos e Configurações nome de usuário Print Username Print \\ \\ Username.                 |
| PROGRAMAS                    | PROGRAMAS                        | Diretório do sistema de arquivos que contém os grupos de programas do usuário (que também são diretórios do sistema de arquivos). Um caminho típico é C: Documentos e Configurações nome de \\ usuário Iniciar Programas de \\ \\ \\ Menu.  |
| PERFIL                     | PERFIL                         | Pasta de perfil do usuário.                                                                                                                                                                 |
| ARQUIVOS DE PROGRAMAS               | PROGRAM%20FILES                 | Pasta Arquivos de Programas. Um caminho típico é C: \\ Arquivos de Programas.                                                                                                                             |
| ARQUIVOS DE PROGRAMAS COMUNS        | PROGRAMFILESCOMMON              | Pasta Arquivos de Programas comum a todos os usuários.                                                                                                                                              |
| ARQUIVOS DE PROGRAMAS COMUNS x86    | PROGRAMFILESCOMMONX86           | Pasta Arquivos de Programas comum a todos os usuários em máquinas x86.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Pasta Arquivos de Programas em máquinas x86.                                                                                                                                                  |
| RECENTE                      | RECENTE                          | Diretório do sistema de arquivos que contém os documentos usados mais recentemente pelo usuário. Um caminho típico é C: Documentos \\ e Configurações nome de usuário \\ \\ Recente.                                           |
| PASTA LIXEIRA          | RECYCLEBINFOLDER                | Pasta virtual que contém os objetos na conta do usuário Lixeira.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | O Diretório de recursos.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Diretório do sistema de arquivos que contém itens de menu Enviar para. Um caminho típico é C: \\ Documentos e Configurações nome de usuário \\ \\ SendTo.                                                                |
| MENU INICIAR                  | START%20MENU                    | Diretório do sistema de arquivos que contém menu Iniciar itens. Um caminho típico é C: Documentos e Configurações \\ menu Iniciar nome de \\ \\ usuário.                                                                 |
| INICIALIZAÇÃO                     | INICIALIZAÇÃO                         | Diretório do sistema de arquivos que corresponde ao grupo de programas de inicialização do usuário.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Pasta do sistema em máquinas x86.                                                                                                                                                         |
| MODELOS                   | MODELOS                       | Diretório do sistema de arquivos que serve como um repositório comum para modelos de documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Pasta do sistema. Um caminho típico é C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows diretório ou SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informações de argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



