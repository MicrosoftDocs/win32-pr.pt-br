---
description: este tópico descreve os itens que Windows índices de pesquisa.
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

este tópico descreve os itens que Windows índices de pesquisa.

Este tópico é organizado da seguinte maneira:

-   [Indexado por padrão](#indexed-by-default)
-   [Formatos de arquivo com suporte](#file-formats-supported)
-   [Exclusões de arquivo](#file-exclusions)
-   [Exclusões de pastas](#folder-exclusions)
-   [Exclusões de unidade](#drive-exclusions)
-   [Tópicos relacionados](#related-topics)

 

## <a name="indexed-by-default"></a>Indexado por padrão

os manipuladores de protocolo e os filtros são incluídos na pesquisa Windows para indexar os seguintes tipos de conteúdo:

-   no Windows Vista e posterior, os itens de email do microsoft Outlook do usuário e do microsoft Outlook Express são indexados enquanto o aplicativo de email está em execução.
-   os arquivos Offline no cache do lado do cliente (CSC) são indexados por Windows pesquisa localmente.
-   Windows A pesquisa dá suporte à coleta de endereços de início de arquivo em volumes NTFS e FAT32. O NTFS dá suporte à indexação baseada em notificação e o FAT32 dá suporte a um rastreamento incremental na inicialização e, em seguida, responde às notificações.
-   Windows O Vista e posteriores continuam a expor uma propriedade por pasta/por arquivo para habilitar a indexação: a opção "**para pesquisa rápida, permitindo que o serviço de indexação indexe esta pasta**" na caixa de diálogo de **Propriedades** . Definir o sinalizador de bits de forma estranha garante que as propriedades básicas do protocolo, como URL, nome de arquivo e tamanho, sejam indexadas, mas que nenhum manipulador de filtro nem manipuladores de propriedade sejam executados.
-   O conteúdo do texto é indexado, mas a pontuação não é.

## <a name="file-formats-supported"></a>Formatos de arquivo com suporte

Windows A pesquisa tem manipuladores de protocolo, manipuladores de propriedade e manipuladores de filtro para indexar os seguintes formatos automaticamente:

-   Arquivos de mídia: todos os tipos de arquivo de mídia
-   **HTML** (nlhtml.dll):. ascx,. asp,. aspx,. CSS,. hhc, .htm, .html,. htt,. htw,. htx,. odc,. stm
-   **HTML MIME** (mimefilt.dll):. mht,. mhtml
-   **Office** (offfilt.dll): .doc,. dot,. pot,. pps, .ppt,. xlb,. xlc, .xls,. xlt
-   **Texto** (query.dll):. asm,. asx, .bat,. c,. cmd,. cpp,. cxx,. def,. dic,. h,. HPP,. hXX,. idl,. idq,. inf, .ini,. inx, .js,. log,. m3u,. rc,. reg,. rtf, .txt,. URL,. vbs,. WTX
-   **XML** (xmlfilt.dll): .xml,. xsl
-   **OneNote**:. One
-   **Diário do Tablet** (jntfiltr.dll):. jnt

As propriedades são indexadas para todos os arquivos, exceto o armazenamento estruturado. no Windows Vista e posterior, muitas propriedades de arquivo de mídia são indexadas; no entanto, o conteúdo não será indexado se os arquivos forem protegidos pelo DRM (gerenciamento de direitos digitais).

> [!Note]  
> O filtro HTML não indexa comentários HTML.

 

## <a name="file-exclusions"></a>Exclusões de arquivo

Quando um tipo de arquivo não tem um filtro associado, ou quando um arquivo não tem uma extensão, as propriedades do sistema para arquivos desse tipo são indexadas, mas o conteúdo do arquivo não é indexado.

além disso, Windows pesquisa não indexa o conteúdo de arquivos em gerenciamento de direitos de informação (IRM) ou DRM (gerenciamento de direitos digitais).

no Windows Vista (somente), os seguintes arquivos são excluídos da indexação por padrão:

-   Arquivos marcados como ocultos ou do sistema.
-   Arquivos com as seguintes extensões:

    .386,. APS,. AudioCD,. bin,. Bk1,. bk2,. bkf,. BSC,. BTR,. chk,. CI,. crwl,. dbg,. DCT,. DeskLink,. dir,. dl \_ , .dll,. drv,. DVD,. evt,. ex \_ , .exe,. exp,. EYB,. fnd,. fnt,. Pasta,. Fon,. GHI,. gthr,. hqx,. ICM,. idb,. idx,. ilk,. IMC,. in \_ , .ini,. inv,. JBF,. LaTeX,. lib,. local,. M14,. Mac,. manifest,. map,. MAPIMail,. MMF,. Movie,. MV,. mydocs,. NCB,. obj,. oC \_ ,. ocx,. pch,. pdb,. PF,. PMA,. PMC,. PML,. PMR,. res,. RMP,. RPC,. rsp,. SBR,. SC2,. sit,. Sr \_ ,. Sy \_ ,. sym, .sys,. tlb,. trc,. TTC,. ttf,. VBX,. vxd,. wll,. WLT,. XIX,. Z96,. ZFSendToTarget.

## <a name="folder-exclusions"></a>Exclusões de pastas

> [!TIP]
> Os nomes de pastas não diferenciam maiúsculas de minúsculas.

 

As seguintes pastas são excluídas da indexação por padrão:



| Padrão de exclusão de pasta                                                              | efeito no Windows 7 | efeito no Windows Vista | Descrição                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% System%* \\ ProgramData \\ \\ dados de pesquisa da Microsoft \\\\                                    | **Excluído**        | Sem efeito               | Dados do indexador na unidade do sistema.                                                                                                                                                                                          |
| *% System%* \\ Usuários \\ *nome de usuário* \\ AppData\\                                              | **Excluído**        | Sem efeito               | Dados de aplicativo do usuário (inclui dados temporários) na unidade do sistema.<br/> Para cada usuário que faz logon no sistema, é adicionado um padrão de exclusão específico que exclui os dados do aplicativo do índice.<br/> |
| *% System%* \\ usuários de \\ \* \\ AppData \\ Local da \\ Microsoft \\ Windows \\ arquivos de Internet temporários\\ | **Excluído**        | Sem efeito               | local padrão de Windows arquivos temporários da internet do internet Explorer na unidade do sistema.<br/> Se o local dos arquivos temporários da Internet do Internet Explorer for alterado, esses arquivos poderão ser indexados.<br/>    |
| *% System%* \\ Windows \\ CSC\\                                                            | **Excluído**        | Sem efeito               | se a indexação estiver ativada para o diretório do sistema Windows, a pasta CSC (na unidade do sistema) ainda será excluída da indexação.                                                                                           |
| *% System%* \\ \\ \* Windows \\ Temp\\                                                       | **Excluído**        | Sem efeito               | Windows dados temporários na unidade do sistema.                                                                                                                                                                                     |
| *% System%* \\ Windows.\*\\                                                              | **Excluído**        | Sem efeito               | instalações de Windows antigas na unidade do sistema.                                                                                                                                                                             |
| *% System%* \\ ProgramData\\                                                             | **Excluído**        | **Excluído**            | Observe que a subpasta do menu iniciar compartilhado é indexada.                                                                                                                                                                     |
| *% System%* \\ Usuários \\ \* \\ AppData\\                                                      | **Excluído**        | **Excluído**            | Dados de aplicativo dos usuários (inclui dados temporários).                                                                                                                                                                              |
| *% System%* \\ Usuários de \\ \* \\ AppData \\ local \\ temporário\\                                         | **Excluído**        | **Excluído**            | Dados temporários dos usuários. Se a indexação estiver ativada para dados de aplicativo do usuário, os dados temporários do usuário ainda serão excluídos da indexação por padrão.                                                                                           |
| *% System%* \\ Windows\\                                                                 | **Excluído**        | **Excluído**            | Arquivos do sistema operacional na unidade do sistema.                                                                                                                                                                                |
| *% System%* \\ $Recycle Bin\\                                                            | **Excluído**        | **Excluído**            | Local dos arquivos na lixeira.                                                                                                                                                                                      |
| *% System%* \\ Integrado\\                                                                   | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Repositório instalado\\                                                    | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Arquivos de programas\\                                                           | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Arquivos de programas (x86)\\                                                     | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Sem efeito           | **Excluído**            | Windows dados temporários e outras pastas com o nome "temp".                                                                                                                                                                  |
| *% System%* \\ Usuários \\ padrão\\                                                          | Sem efeito           | **Excluído**            | O local dos dados de perfil de usuário padrão na unidade do sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Sem efeito           | **Excluído**            | instalações antigas de Windows e outras pastas com nomes que começam com "Windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusões de unidade

no Windows 7 e no Windows Vista, as unidades removíveis não são indexadas por padrão.

> [!Note]  
> Se as unidades removíveis se reportarem como unidades fixas, você poderá adicioná-las a serem indexadas mesmo que elas sejam realmente removíveis. as informações permanecerão no índice e Windows pesquisa fará um rastreamento incremental para reconciliar os resultados de indexação quando o disco removível for conectado novamente. Como as unidades flash USB se reportam como removíveis, elas não podem ser indexadas.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[indexação, consulta e notificações na pesquisa Windows](-search-3x-wds-included-in-index.md)
</dt> <dt>

[processo de indexação na pesquisa Windows](-search-indexing-process-overview.md)
</dt> <dt>

[processo de consulta na pesquisa Windows](querying-process--windows-search-.md)
</dt> <dt>

[processo de notificações na pesquisa Windows](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formatação de URL](url-formatting-requirements.md)
</dt> </dl>

 

 




