---
description: Se, após a execução de uma instalação, você precisar verificar se um recurso, componente ou arquivo específico foi instalado, ative a opção de log detalhado durante a instalação. Consulte Windows Installer opções de registro em log e linha de comando.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Verificando a instalação de recursos, componentes, arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748783"
---
# <a name="checking-the-installation-of-features-components-files"></a>Verificando a instalação de recursos, componentes, arquivos

Se, após a execução de uma instalação, você precisar verificar se um recurso, componente ou arquivo específico foi instalado, ative a opção de log detalhado durante a instalação. Consulte [Windows Installer](windows-installer-logging.md) opções de registro em log e [linha de comando](command-line-options.md).

O log detalhado inclui uma entrada para cada recurso e componente que o pacote de instalação pode instalar. O log informa qual é o estado desse recurso ou componente antes da instalação, qual estado foi solicitado pela instalação e em que estado o instalador deixou o recurso ou componente. As entradas de componente e recurso no log aparecem como os exemplos a seguir.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Esse log detalhado indica que:

-   o estado de instalação do recurso QuickTest e do componente estava ausente antes da execução do pacote
-   o pacote solicitou uma instalação local desses
-   o recurso e o componente foram ambos deixados no estado instalado localmente após a execução do pacote.

O rótulo "instalado" no log refere-se ao estado de instalação atual do recurso ou componente, "solicitação" refere-se ao estado de instalação solicitado do recurso ou componente. "Action" refere-se ao estado de ação real do recurso ou componente.

A tabela a seguir lista os possíveis estados de componente ou recurso que podem aparecer no log.



| Entrada de Log              | Descrição                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Solicitação: nula          | Nenhuma solicitação.                                                                                                     |
| Ação: nulo           | Nenhuma ação executada.                                                                                                |
| Instalado: ausente      | O componente ou recurso não está instalado no momento.                                                                |
| Solicitação: ausente        | O componente ou recurso de solicitações de instalação será desinstalado.                                                      |
| Ação: ausente         | O instalador realmente desinstala o componente ou recurso.                                                             |
| Instalado: local       | O componente ou recurso está instalado no momento para executar o local.                                                       |
| Solicitação: local         | O componente ou o recurso de solicitações de instalação deve ser instalado para executar o local.                                           |
| Ação: local          | Na verdade, o instalador instala o componente ou recurso para executar o local.                                                  |
| Instalado: origem      | O componente ou recurso está atualmente instalado para ser executado da origem.                                                 |
| Solicitado: fonte      | A instalação solicita que o componente ou o recurso seja instalado para ser executado da origem.                                |
| Ação: origem         | Na verdade, o instalador instala o componente ou o recurso a ser executado da origem.                                        |
| Instalado: anunciar   | O recurso está anunciado no momento. Os componentes nunca são anunciados.                                               |
| Solicitação: anunciar     | O recurso de solicitações de instalação é instalado como um recurso anunciado.                                            |
| Ação: anunciar      | Na verdade, o instalador instala o recurso como um recurso anunciado.                                               |
| Solicitação: reinstalar     | O recurso de solicitações de instalação será reinstalado. Os componentes não usam o estado de reinstalação.                            |
| Ação: reinstalar      | O instalador realmente reinstala o recurso.                                                                          |
| Instalado: atual     | O recurso está atualmente instalado no estado de instalação criado padrão.                                           |
| Solicitação: atual       | O recurso de solicitações de instalação é instalado no estado de instalação de criação padrão.                               |
| Ação: atual        | Na verdade, o instalador instala o recurso no estado de instalação criado por padrão.                                  |
| Ação: fileausente     | O instalador realmente desinstala os arquivos do componente e deixa todos os outros recursos do componente instalados.      |
| Ação: HKCRAbsent     | Na verdade, o instalador remove as informações de HKCR do componente. As informações de arquivo e não de HKCR permanecem.                  |
| Ação: HKCRFileAbsent | Na verdade, o instalador remove as informações e os arquivos de HKCR do componente. Todos os outros recursos do componente permanecem. |



 

O log detalhado tem uma entrada para cada arquivo que pode ser instalado pelo pacote. O log informa o que foi feito ao arquivo e fornece algumas explicações. As entradas de arquivo no log aparecem como no exemplo a seguir.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Esse log indica que o instalador não substituirá o arquivo de Testdb.exe existente, pois o arquivo existente é o mesmo que a versão que está sendo instalada.

> [!Note]  
> Se você precisar criar um pacote de instalação que pesquise um arquivo ou diretório existente no computador do usuário durante uma instalação, use o método descrito em [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

 

 

 



