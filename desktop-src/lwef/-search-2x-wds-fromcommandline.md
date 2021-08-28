---
title: Chamando o WDS da linha de comando
description: Você pode iniciar a interface do usuário do WDS (Pesquisa de Área de Trabalho do Microsoft Windows) com um filtro, armazenamento e consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (Objeto Auxiliar do Navegador) usando a sintaxe de linha de comando windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0125d9c4733654df7b2f6e08f49d10f5fee07
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467603"
---
# <a name="calling-wds-from-the-command-line"></a>Chamando o WDS da linha de comando

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para o Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

Você pode iniciar a interface do usuário do WDS (Pesquisa de Área de Trabalho do Microsoft Windows) com um filtro, armazenamento e consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (Objeto Auxiliar do Navegador) usando a sintaxe de linha de comando windowssearch.exe. Ao chamar o WDS da linha de comando, nenhuma informação sobre as ações ou a seleção do usuário na janela do WDS é retornada para o aplicativo de chamada ou a página da Web.

O caminho de instalação do WDS é especificado na configuração do Registro InstallDir em HKEY_LOCAL_MACHINE \\ Software Microsoft Windows Desktop \\ \\ Search. O caminho padrão para o windowssearch.exe está instalado é Arquivos de Programas \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

A sintaxe a seguir se aplica à interface de linha de comando Windows Desktop Search 2.x.




| Opções | Parâmetro | Significado | 
|---------|-----------|---------|
| /startup | Inicializa a pesquisa Windows Área de Trabalho | 
| /indexnow | Desliga o back-off de indexação e pesquisa novamente todos os locais de índice | 
| /showstatus | Mostra a janela de status de indexação | 
| /launchsearchwindow ou /url | Abre uma janela do WDS com uma consulta vazia | 
| /url | search:[store|show|query] query string | Abre uma janela do WDS com uma consulta e um filtro com base nos seguintes parâmetros:<ul><li><p>store – especifica a fonte de dados a ser consultada: arquivos, outlook, outlookexpress. Se não for especificado, todos os armazenamentos serão pesquisados. <br /></p><blockquote>[!Note]<br />Embora a Sintaxe de Consulta Avançada seja compatível com a referência do Microsoft Outlook como 'oe', o parâmetro store na linha de comando deve ser 'outlookexpress'.</blockquote><p><br /></p></li><li><p>show – especifica qual tipo percebido de resultados retornar. Consulte <a href="-search-2x-wds-perceivedtype.md">Tipos percebidos</a> para ver uma lista completa de tipos. Se não for especificado, todos os tipos serão retornados. <br /></p><blockquote>[!Note]<br />Há três diferenças entre os valores de tipo percebidos e os valores para show. Para , use 'documents' em vez de 'doc', 'pictures' em vez de <code>show</code> 'pics' e 'textdocuments' em vez de 'text'.</blockquote><p><br /></p></li><li>consulta – especifica os critérios de pesquisa. Esse valor dá <a href="-search-2x-wds-aqsreference.md">suporte a parâmetros de Sintaxe de</a> Consulta Avançada para refinar os resultados. O parâmetro de consulta deve ser o último parâmetro na URL.</li></ul> | 




 

## <a name="example"></a>Exemplo

Por exemplo, para pesquisar imagens correspondentes aos critérios 'papel de parede' em todos os arquivos, use o seguinte comando:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percebidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





