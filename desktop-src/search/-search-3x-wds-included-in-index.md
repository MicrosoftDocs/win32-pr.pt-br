---
description: Este tópico descreve os itens que Windows Pesquisar.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: O que está incluído no índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbffec8aba8a985faca112eac434b669d22eff82d94d6b4eaf5588585ced771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463319"
---
# <a name="what-is-included-in-the-index"></a>O que está incluído no índice

Este tópico descreve os itens que Windows Pesquisar.

Este tópico é organizado da seguinte forma:

-   [Indexado por padrão](#indexed-by-default)
-   [Formatos de arquivo com suporte](#file-formats-supported)
-   [Exclusões de arquivo](#file-exclusions)
-   [Exclusões de pasta](#folder-exclusions)
-   [Exclusões de unidade](#drive-exclusions)
-   [Tópicos relacionados](#related-topics)

 

## <a name="indexed-by-default"></a>Indexado por padrão

Manipuladores de protocolo e filtros são incluídos Windows Search para indexar os seguintes tipos de conteúdo:

-   No Windows Vista e posterior, os itens Microsoft Outlook e Microsoft Outlook Express mail de um usuário são indexados enquanto o aplicativo de email está em execução.
-   Arquivos offline no CSC (cache do lado do cliente) são indexados por Windows Search localmente.
-   Windows A pesquisa dá suporte à coleta de endereços de início de arquivo em volumes NTFS e FAT32. O NTFS dá suporte à indexação baseada em notificação e o FAT32 dá suporte a um rastreamento incremental na início e, em seguida, responde às notificações.
-   Windows O Vista e posterior continuam a expor uma propriedade por pasta/por arquivo para habilitar a indexação: a opção " Para pesquisa **rápida,** permitindo que o Serviço de Indexação indexe essa pasta " na caixa **de** diálogo Propriedade . Definir o sinalizador de bits FANCI garante que as propriedades básicas do protocolo, como URL, nome de arquivo e tamanho, sejam indexadas, mas que nenhum manipulador de filtro nem manipuladores de propriedade sejam executados.
-   O conteúdo do texto é indexado, mas a pontuação não.

## <a name="file-formats-supported"></a>Formatos de arquivo com suporte

Windows A pesquisa tem manipuladores de protocolo, manipuladores de propriedades e manipuladores de filtro para indexar os seguintes formatos automaticamente:

-   Arquivos de mídia: todos os tipos de arquivo de mídia
-   **HTML** (nlhtml.dll): .ascx, .asp, .aspx, .css, .hhc, .htm, .html, .htt, .htw, .htx, .odc, .stm
-   **MIME HTML** (mimefilt.dll): .mht, .mhtml
-   **Office** (offfilt.dll): .doc, .dot, .pot, .pps, .ppt, .xlb, .xlc, .xls, .xlt
-   **Texto** (query.dll): .asm, .asx, .bat, .c, .cmd, .cpp, .cxx, .def, .dic, .h, .hpp, .hxx, .idl, .idq, .inf, .ini, .inx, .js, .log, .m3u, .rc, .reg, .rtf, .txt, .url, .vbs, .wtx
-   **XML** (xmlfilt.dll): .xml, .xsl
-   **OneNote:**.one
-   **Tablet Journal** (jntfiltr.dll): .jnt

As propriedades são indexadas para todos os arquivos, exceto o armazenamento estruturado. No Windows Vista e posterior, muitas propriedades de arquivo de mídia são indexadas; no entanto, o conteúdo não será indexado se os arquivos são protegidos pelo DRM (gerenciamento de direitos digitais).

> [!Note]  
> O filtro HTML não indexa comentários HTML.

 

## <a name="file-exclusions"></a>Exclusões de arquivo

Quando um tipo de arquivo não tem um filtro associado ou quando um arquivo não tem uma extensão, as propriedades do sistema para arquivos desse tipo são indexadas, mas o conteúdo do arquivo não é indexado.

Além disso, Windows Search não indexa o conteúdo dos arquivos em IRM (gerenciamento de direitos de informação) ou DRM (gerenciamento de direitos digitais).

No Windows Vista (somente), os seguintes arquivos são excluídos da indexação por padrão:

-   Arquivos marcados como Oculto ou Sistema.
-   Arquivos com as seguintes extensões:

    .386, .aps, . AudioCD, .bin, .bk1, .bk2, .bkf, .bsc, .btr, .chk, .ci, .crwl, .dbg, .dct, . DeskLink, .dir, .dl, \_ .dll, .drv, .dvd, .evt, .ex \_ , .exe, .exp, .eyb, .fnd, .fnt, . Folder, .fon, .gee, .gthr, .hqx, .icm, .idb, .idx, .ilk, .imc, .in \_ , .ini, .inv, .jbf, .latex, .lib, .local, .m14, .mac, .manifest, .map, . MAPIMail, .mmf, .movie, .mv, .mydocs, .ncb, .obj, .oc \_ , .ocx, .pch, .pdb, .pf, .pma, .pmc, .pml, .pmr, .res, .rmp, .rpc, .rsp, .sbr, .sc2, .sit, .sr \_ , .sy, \_ .sym, .sys, .tlb, .trc, .ttc, .ttf, .vbx, .vxd, .wll, .wlt, .sym, .tlb, .z96, . ZFSendToTarget.

## <a name="folder-exclusions"></a>Exclusões de pasta

> [!TIP]
> Os nomes de pastas não são sensíveis a minúsculas.

 

As seguintes pastas são excluídas da indexação por padrão:



| Padrão de exclusão de pasta                                                              | Efeito na Windows 7 | Efeito no Windows Vista | Descrição                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *%System%* \\ ProgramData \\ Microsoft \\ Search \\ Data\\                                    | **Excluído**        | Sem efeito               | Dados do indexador na unidade do sistema.                                                                                                                                                                                          |
| *%System%* \\ UserName \\ *AppData dos* \\ usuários\\                                              | **Excluído**        | Sem efeito               | Os dados do aplicativo do usuário (inclui dados temporários) na unidade do sistema.<br/> Para cada usuário que faz login no sistema, é adicionado um padrão de exclusão específico que exclui os dados do aplicativo do índice.<br/> |
| *%System%* \\ Usuários \\ \* \\ AppData \\ Local Microsoft Windows arquivos \\ \\ \\ temporários da Internet\\ | **Excluído**        | Sem efeito               | Local padrão de Windows Internet Explorer arquivos temporários da Internet na unidade do sistema.<br/> Se o local de Internet Explorer arquivos temporários da Internet for alterado, esses arquivos poderão ser indexados.<br/>    |
| *%System%* \\ \\Windows Csc\\                                                            | **Excluído**        | Sem efeito               | Se a indexação estiver Windows diretório do sistema, a pasta CSC (na unidade do sistema) ainda será excluída da indexação.                                                                                           |
| *%System%* \\ \\ \* Windows \\ Temp\\                                                       | **Excluído**        | Sem efeito               | Windows dados temporários na unidade do sistema.                                                                                                                                                                                     |
| *%System%* \\ Windows.\*\\                                                              | **Excluído**        | Sem efeito               | Instalações Windows antigas na unidade do sistema.                                                                                                                                                                             |
| *%System%* \\ Programdata\\                                                             | **Excluído**        | **Excluído**            | Observe que a sub pasta Menu Iniciar compartilhado está indexada.                                                                                                                                                                     |
| *%System%* \\ AppData \\ \* \\ dos usuários\\                                                      | **Excluído**        | **Excluído**            | Dados do aplicativo dos usuários (inclui dados temporários).                                                                                                                                                                              |
| *%System%* \\ Temp \\ \* \\ local appData dos \\ \\ usuários\\                                         | **Excluído**        | **Excluído**            | Dados temporários dos usuários. Se a indexação estiver 1000% 10000011, os dados temporários do usuário ainda serão excluídos da indexação por padrão.                                                                                           |
| *%System%* \\ Windows\\                                                                 | **Excluído**        | **Excluído**            | Arquivos do sistema operacional na unidade do sistema.                                                                                                                                                                                |
| *%System%* \\ $Lixeira\\                                                            | **Excluído**        | **Excluído**            | Local dos arquivos no Lixeira.                                                                                                                                                                                      |
| *%System%* \\ Construir\\                                                                   | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *%System%* \\ Repositório instalado\\                                                    | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *%System%* \\ Arquivos de Programas\\                                                           | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *%System%* \\ Arquivos de Programas (x86)\\                                                     | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Sem efeito           | **Excluído**            | Windows dados temporários e outras pastas com o nome "temp".                                                                                                                                                                  |
| *%System%* \\ Padrão de \\ usuários\\                                                          | Sem efeito           | **Excluído**            | O local dos dados de perfil do usuário padrão na unidade do sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Sem efeito           | **Excluído**            | Instalações Windows antigas e outras pastas com nomes que começam com "windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusões de unidade

No Windows 7 e Windows Vista, as unidades removíveis não são indexadas por padrão.

> [!Note]  
> Se as unidades removíveis se reportarem como unidades fixas, você poderá adicioná-las para serem indexadas mesmo que elas sejam realmente removíveis. As informações permanecerão no índice e Windows Search fará um rastreamento incremental para reconciliar os resultados da indexação quando o disco removível estiver conectado novamente. Como as unidades flash USB se reportam como removíveis, elas não podem ser indexadas.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Processo de indexação na Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de consulta na Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Processo de notificações na Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formatação de URL](url-formatting-requirements.md)
</dt> </dl>

 

 




