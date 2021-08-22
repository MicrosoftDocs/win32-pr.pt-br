---
description: Se, depois de executar uma instalação, você precisar verificar se um determinado recurso, componente ou arquivo foi instalado, a ligue a opção de registro em log detalhado durante a instalação. Consulte Windows log do instalador e opções de linha de comando.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Verificando a instalação de recursos, componentes, arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866b4f7b042c97660e43a92fc55eeb99e2f1e9f3574a9b03c4d3d6e6096504c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145599"
---
# <a name="checking-the-installation-of-features-components-files"></a>Verificando a instalação de recursos, componentes, arquivos

Se, depois de executar uma instalação, você precisar verificar se um determinado recurso, componente ou arquivo foi instalado, a ligue a opção de registro em log detalhado durante a instalação. Consulte [as Windows log do instalador e](windows-installer-logging.md) opções de linha de [comando](command-line-options.md).

O log detalhado inclui uma entrada para cada recurso e componente que o pacote de instalação pode instalar. O log informa qual era o estado desse recurso ou componente antes da instalação, qual estado foi solicitado pela instalação e em que estado o instalador deixou o recurso ou componente. As entradas de recurso e componente no log aparecem como os exemplos a seguir.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Esse log detalhado indica que:

-   o estado de instalação do recurso e do componente QuickTest estava ausente antes de executar o pacote
-   o pacote solicitou uma instalação local desses
-   o recurso e o componente foram deixados no estado instalado localmente depois de executar o pacote.

O rótulo "Instalado" no log refere-se ao estado de instalação atual do recurso ou componente, "Solicitação" refere-se ao estado de instalação solicitado do recurso ou componente. "Action" refere-se ao estado de ação real do recurso ou componente.

A tabela a seguir lista os possíveis estados de componente ou recurso que podem aparecer no log.



| Entrada de Log              | Descrição                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Solicitação: Nulo          | Nenhuma solicitação.                                                                                                     |
| Ação: Nulo           | Nenhuma ação realizada.                                                                                                |
| Instalado: Ausente      | O componente ou o recurso não está instalado no momento.                                                                |
| Solicitação: Ausente        | Componente ou recurso de solicitações de instalação a ser desinstalado.                                                      |
| Ação: Ausente         | Na verdade, o instalador desinstala o componente ou o recurso.                                                             |
| Instalado: Local       | O componente ou o recurso está atualmente instalado para ser executado localmente.                                                       |
| Solicitação: Local         | Componente ou recurso de solicitações de instalação a ser instalado para executar localmente.                                           |
| Ação: Local          | Na verdade, o instalador instala o componente ou o recurso para executar localmente.                                                  |
| Instalado: Origem      | O componente ou o recurso está atualmente instalado para ser executado da origem.                                                 |
| Solicitado: Origem      | A instalação solicita que esse componente ou recurso seja instalado para ser executado da origem.                                |
| Ação: origem         | Na verdade, o instalador instala o componente ou o recurso a ser executado da origem.                                        |
| Instalado: Anunciar   | O recurso é anunciado no momento. Os componentes nunca são anunciados.                                               |
| Solicitação: Anunciar     | O recurso de solicitações de instalação é instalado como um recurso anunciado.                                            |
| Ação: Anunciar      | Na verdade, o instalador instala o recurso como um recurso anunciado.                                               |
| Solicitação: Reinstalar     | O recurso de solicitações de instalação será reinstalado. Os componentes não usam o estado de reinstalação.                            |
| Ação: Reinstalar      | Na verdade, o instalador reinstala o recurso.                                                                          |
| Instalado: Atual     | No momento, o recurso está instalado no estado de instalação padrão.                                           |
| Solicitação: Atual       | O recurso de solicitações de instalação é instalado no estado de instalação padrão.                               |
| Ação: Atual        | Na verdade, o instalador instala o recurso no estado de instalação padrão.                                  |
| Ação: FileAbsent     | Na verdade, o instalador desinstala os arquivos do componente e deixa todos os outros recursos do componente instalados.      |
| Ação: HKCRAbsent     | Na verdade, o instalador remove as informações de HKCR do componente. As informações de arquivo e não HKCR permanecem.                  |
| Ação: HKCRFileAbsent | Na verdade, o instalador remove as informações e os arquivos HKCR do componente. Todos os outros recursos do componente permanecem. |



 

O log detalhado tem uma entrada para cada arquivo que pode ser instalado pelo pacote. O log informa o que foi feito no arquivo e fornece alguma explicação. As entradas de arquivo no log aparecem como no exemplo a seguir.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Esse log indica que o instalador não substituirá o arquivo Testdb.exe existente porque o arquivo existente é o mesmo que a versão que está sendo instalada.

> [!Note]  
> Se você precisar autor de um pacote de instalação que pesquise um arquivo ou diretório existente no computador do usuário durante uma instalação, use o método descrito em Pesquisando aplicativos [existentes, arquivos,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)entradas de registro ou entradas de arquivo .ini .

 

 

 



