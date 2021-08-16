---
description: Entenda como usar o argumento DECOD NA interface do usuário Windows Shell como um meio de controlar o escopo de uma pesquisa.
title: Argumento DEM (o shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b93764f8014a5d9446811ef622f7c5afc20acbc6193d938c98642afaae5392fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452872"
---
# <a name="crumb-argument-the-windows-shell"></a>Argumento DEM (o shell Windows)

O argumento dá suporte a instruções completas de `crumb` AQS (Advanced Query Syntax) e é especialmente útil como um meio de controlar o escopo de uma pesquisa. Além das instruções do AQS, o argumento pode usar um parâmetro especial no Windows Vista e nos `crumb` `location` `kind` parâmetros Windows XP, conforme descrito posteriormente `store` neste tópico.

Este tópico contém as seguintes seções:

-   [Sintaxe de sintaxe de sintaxe de sintaxe](#crumb-syntax)
    -   [Exemplos gerais](#general-examples)
-   [Usando o mofando com o Vista (localização)](#using-crumb-with-vista-location)
    -   [Exemplos do Vista](#vista-examples)
    -   [Constantes para pastas comuns](#constants-for-common-folders)
    -   [Informações de argumento](#argument-information)

## <a name="crumb-syntax"></a>Sintaxe de sintaxe de sintaxe de sintaxe

A sintaxe de sintaxe de sintaxe é a seguinte:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



A <column> parte é qualquer propriedade no sistema de propriedades e o <value> parte é um valor válido para essa propriedade. A <label> parte é um alias opcional para a propriedade que é exibida como uma dica de interface do usuário.

### <a name="general-examples"></a>Exemplos gerais


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Usando o mofando com o Vista (localização)

No parâmetro de sistema, Windows Vista dá suporte ao AQS completo e também à propriedade , que tem uma implementação especial disponível somente no `location` Windows Vista. Você pode usar uma cadeia de caracteres do AQS ou a propriedade dentro de um único parâmetro `location` de controle, mas não ambos. Se o parâmetro de desatrelação incluir o AQS, todo o resto nesse parâmetro de desatrelação será ignorado.

A `location` propriedade permite que você especifique um caminho a ser pesquisado. Windows O Vista poderá ignorar o Indexador e percorrer o diretório diretamente se o local estiver fora do escopo de rastreamento do Indexador. Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o Indexador.

Quando você especifica uma `location` propriedade, há suporte para dois parâmetros adicionais e opcionais:



| Parâmetro | Valores                  | Descrição                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inclusão | incluir, excluir        | Especifica se a consulta deve incluir ou excluir itens desse caminho. "Incluir" é o padrão. Windows O Vista não dá suporte a exclusões sem inclusões. (Veja o exemplo) |
| recursão | recursivo, não recursivo | Especifica se a pesquisa deve recursar todas as subpastas começando com o valor definido no local:<value>. "Recursivo" é o padrão.                             |



 

Para escopo de uma pesquisa usando **o protocolo search:,** você tem opções diferentes, dependendo do destino do escopo.

Pasta em um computador local:

-   Usar o AQS (folder=folder:<caminho codificado por URL>)
-   Use o argumento location (encode=location:<caminho codificado por URL>)

Pasta em um computador/rede remoto:

-   Use o argumento location (encode=location:<caminho codificado por URL>)

Pasta acessada por meio de um manipulador de protocolo UNC (Convenção Universal de Nomenização) conhecido:

-   Usar o AQS (agora= store: <UNC protocol handler name> )
-   Use o argumento location (encode=location:<caminho codificado por URL>)

### <a name="vista-examples"></a>Exemplos do Vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



O primeiro exemplo executa uma pesquisa de "férias" começando no local (um atalho especial para a pasta Meus Documentos do usuário), incluindo essa pasta e todas as `shell://Personal` subpastas.  Consulte a tabela abaixo.

O segundo exemplo executa uma pesquisa em C: \\ Imagens, mas não em C: \\ \\ Duplicatas de Imagens.

O terceiro exemplo executa uma pesquisa em C: Documentos, limitado a arquivos com a \\ `kind` propriedade definida como imagens.

### <a name="constants-for-common-folders"></a>Constantes para pastas comuns

Windows O Vista permite o uso de valores CSIDL que fornecem uma maneira exclusiva independente do sistema para identificar pastas especiais usadas com frequência por aplicativos, mas que podem não ter o mesmo nome ou local em qualquer sistema específico. Por exemplo, a pasta do sistema pode ser "C: Windows" em um \\ sistema e "C: \\ Winnt" em outro.

Use estes locais com esta sintaxe:


```
crumb=location:shell%3a<LocationName>&
```



A tabela a seguir lista os valores CSIDL. Consulte [**ShellSpecialFolderConstants para**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) obter mais informações.



| Nome                        | cadeia de caracteres de pesquisa                   | Descrição                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FERRAMENTAS ADMINISTRATIVAS        | ADMINISTRATIVE%20TOOLS          | Diretório do sistema de arquivos que serve como um repositório para ferramentas administrativas.                                                                                                            |
| APPDATA                     | APPDATA                         | Diretório do sistema de arquivos que serve como um repositório comum para dados específicos do aplicativo. Um caminho típico é C: documentos \\ e Configurações dados do aplicativo de nome de \\ \\ usuário.                      |
| CACHE                       | CACHE                           | Diretório do sistema de arquivos que serve como um repositório comum para arquivos temporários da Internet. Um caminho típico é C: documentos \\ e Configurações nome de usuário \\ \\ Temporários da Internet.               |
| CD DE GRAVAÇÃO                  | CD%20IÃO                    | Pasta que contém dados a serem gravados em CD.                                                                                                                                             |
| FERRAMENTAS ADMINISTRATIVAS COMUNS | COMMON%20ADMINISTRATIVE%20TOOLS | Ferramentas administrativas para todos os usuários.                                                                                                                                                    |
| COMMON APPDATA              | COMMON%20APPDATA                | Dados do aplicativo para todos os usuários. Um caminho típico é C: \\ Documentos e Configurações dados do aplicativo Todos os \\ \\ Usuários.                                                                             |
| ÁREA DE TRABALHO COMUM              | ÁREA DE TRABALHO COMUM                  | Microsoft Windows Desktop para todos os usuários. Pasta virtual que é a raiz do namespace.                                                                                        |
| DOCUMENTOS COMUNS            | COMMON%20DOCUMENTS              | Documentos para todos os usuários. Um caminho típico é C: \\ Documentos e Configurações todos os usuários \\ \\ Meus Documentos.                                                                                        |
| PROGRAMAS COMUNS             | COMMON%20PROGRAMS               | Grupos de programas comuns a todos os usuários. Um caminho típico é C: \\ Documentos e Configurações Todos os Usuários Iniciar Programas de \\ \\ \\ Menu.                                                                     |
| MENU INICIAR COMUM           | COMMON%20START%20MENU           | menu Iniciar itens comuns a todos os usuários. Um caminho típico é C: \\ Documentos e Configurações Menu Iniciar Todos os \\ \\ Usuários.                                                                             |
| INICIALIZAÇÃO COMUM              | COMMON%20STARTUP                | Grupo de programas de inicialização comum a todos os usuários.                                                                                                                                             |
| MODELOS COMUNS            | COMMON%20TEMPLATES              | Modelos de documento comuns a todos os usuários.                                                                                                                                                |
| COMMONMUSIC                 | MY%20MUSIC                      | Modelos de pasta My Music comuns a todos os usuários.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | Modelos de pasta Minhas Imagens comuns a todos os usuários.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Modelos de pasta Meu Vídeo comuns a todos os usuários.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | pasta que contém dados de conexão.                                                                                                                                                     |
| PASTA PAINEL DE CONTROLE        | CONTROLPANELFOLDER              | Pasta virtual que contém ícones para os Painel de Controle aplicativos.                                                                                                                    |
| Cookies                     | Cookies                         | Diretório do sistema de arquivos que serve como um repositório comum para cookies da Internet. Um caminho típico é C: documentos e Configurações \\ cookies de nome de \\ \\ usuário.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Pasta virtual que é a raiz do namespace.                                                                                                           |
| FAVORITOS                   | FAVORITOS                       | Diretório do sistema de arquivos que serve como um repositório comum para os itens favoritos do usuário. Um caminho típico é C: Documentos \\ e Configurações \\ \\ favoritos de nome de usuário.                             |
| Fontes                       | Fontes                           | Pasta virtual que contém fontes instaladas. Um caminho típico é C: \\ \\ Fontes do WINDOWS.                                                                                                       |
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
| ARQUIVOS DE PROGRAMAS COMUNS        | PROGRAMFILESCOMMON              | Pasta arquivos de programas comuns a todos os usuários.                                                                                                                                              |
| ARQUIVOS de programas comuns x86    | PROGRAMFILESCOMMONX86           | Pasta arquivos de programas comuns a todos os usuários em computadores x86.                                                                                                                              |
| FILESx86 do programa            | PROGRAMFILESx86                 | Pasta arquivos de programas em computadores x86.                                                                                                                                                  |
| VERSÕES                      | VERSÕES                          | Diretório do sistema de arquivos que contém os documentos usados mais recentemente do usuário. um caminho típico é C: \\ documents e Configurações \\ nome de usuário \\ recente.                                           |
| PASTA DA LIXEIRA          | RECYCLEBINFOLDER                | Pasta virtual que contém os objetos na lixeira do usuário.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | O diretório de recursos.                                                                                                                                                                |
| Enviar                      | Enviar                          | Diretório do sistema de arquivos que contém itens de menu Enviar para. um caminho típico é C: \\ documents e Configurações \\ nome de usuário \\ SendTo.                                                                |
| MENU INICIAR                  | INICIAR% 20MENU                    | diretório do sistema de arquivos que contém itens de menu Iniciar. um caminho típico é C: \\ documents e Configurações \\ Menu iniciar do nome de usuário \\ .                                                                 |
| INICIALIZAÇÃO                     | INICIALIZAÇÃO                         | Diretório do sistema de arquivos que corresponde ao grupo de programas de inicialização do usuário.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Pasta do sistema em computadores x86.                                                                                                                                                         |
| MODELOS                   | MODELOS                       | Diretório do sistema de arquivos que serve como um repositório comum para modelos de documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Pasta do sistema. um caminho típico é C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows directory ou SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informações do argumento



|                              | Valor                                   |
|------------------------------|-----------------------------------------|
| **Sistema operacional mínimo** | Windows Vista com Service Pack 1 (SP1) |



 

 

 



