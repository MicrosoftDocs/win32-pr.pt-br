---
description: O Windows Installer armazena todas as cadeias de caracteres de banco de dados em um único pool de cadeias compartilhada para reduzir o tamanho do banco de dados e para melhorar o desempenho. Para obter uma lista de páginas de código numérico, consulte Localizando as tabelas Error e ActionText.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Manipulação de página de código (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769325"
---
# <a name="code-page-handling-windows-installer"></a>Manipulação de página de código (Windows Installer)

O Windows Installer armazena todas as cadeias de caracteres de banco de dados em um único pool de cadeias compartilhada para reduzir o tamanho do banco de dados e para melhorar o desempenho. Para obter uma lista de páginas de código numérico, consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md).

Para obter mais informações, [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md).

Windows Installer usa [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) para determinar se a página de código é válida.

### <a name="localizing-a-windows-installer-package"></a>Localizando um pacote de Windows Installer

Se você localizar um pacote de Windows Installer, ele poderá envolver a modificação de informações em tabelas de banco de dados, exportar as tabelas para arquivos de texto ANSI e, em seguida, importar os arquivos mortos para o banco de dados que está sendo localizado. Você também pode adicionar alterações de localização a um banco de dados usando um editor de tabela de banco de dados ou as [funções de banco](database-functions.md)de dados. É importante definir a página de código do banco de dados que está sendo localizado antes de fazer qualquer alteração de localização no banco de dados. Não defina a página de código do banco de dados depois de localizar o banco de dados, pois isso pode corromper os caracteres estendidos. Para obter mais informações, consulte [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md).

A abordagem recomendada para lidar com páginas de código é criar um banco de dados neutro que contenha apenas caracteres que possam ser traduzidos em qualquer página de código. Para obter mais informações, consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md).

Se você adicionar informações de localização com arquivos mortos de banco de dados, poderá usar o [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para exportar tabelas de um banco de dados que contém alterações de localização para arquivos mortos de texto ANSI e, em seguida, importá-las para o banco de dados que está sendo localizado com [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). A página de código de um arquivo morto exportado é sempre igual ao seu banco de dados pai. As páginas de código de um arquivo importado e o banco de dados que está recebendo o arquivo devem ser idênticos ou pelo menos uma das duas páginas de código deve ser neutra. Para obter mais informações, consulte [manipulação de página de código de tabelas importadas e](code-page-handling-of-imported-and-exported-tables.md)exportadas.

Se você adicionar informações de localização com um editor de texto ou as [funções de banco de dados](database-functions.md) , tome cuidado para passar parâmetros de cadeia de caracteres para a API Windows Installer que usa a página de código do banco de dados que está sendo localizado. Se um parâmetro de cadeia de caracteres contiver caracteres não representados pela página de código do banco de dados, ocorrerá um erro ao chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Para obter mais informações, consulte [manipulação de página de código de cadeias de caracteres de parâmetro](code-page-handling-of-parameter-strings.md).

Se um pacote for usado para instalar várias versões de idioma de um produto, a transformação usada para localizar cadeias de caracteres também poderá alterar a página de código do banco de dados.

 

 
