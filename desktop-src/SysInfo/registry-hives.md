---
description: Um hive é um grupo lógico de chaves, subchaves e valores no registro que tem um conjunto de arquivos de suporte que contém backups de seus dados.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Hives do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828681"
---
# <a name="registry-hives"></a>Hives do registro

Um *Hive* é um grupo lógico de chaves, subchaves e valores no registro que tem um conjunto de arquivos de suporte carregados na memória quando o sistema operacional é iniciado ou um usuário faz logon.

Cada vez que um novo usuário faz logon em um computador, um novo hive é criado para esse usuário com um arquivo separado para o perfil do usuário. Isso é chamado de *hive de perfil de usuário*. O hive de um usuário contém informações específicas do Registro referentes às configurações do aplicativo, área de trabalho, ambiente, conexões de rede e impressoras do usuário. Os hives de perfil de usuário estão localizados na chave de **\_ usuários hKey** .

Os arquivos do registro têm os dois formatos a seguir: Standard e mais recente. O formato padrão é o único formato suportado pelo Windows 2000. Ele também é compatível com versões posteriores do Windows para compatibilidade com versões anteriores. O formato mais recente tem suporte a partir do Windows XP. Nas versões do Windows que dão suporte ao formato mais recente, as seções a seguir ainda usam o formato padrão: **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine \\ Sam**, **HKEY \_ local \_ Machine \\ Security** e **HKEY \_ Users \\ . PADRÃO**; todas as outras seções usam o formato mais recente.

A maioria dos arquivos de suporte para os hives está no diretório de configuração% SystemRoot% \\ System32 \\ . Esses arquivos são atualizados cada vez que um usuário faz logon. As extensões de nome de arquivo dos arquivos nesses diretórios ou, em alguns casos, uma falta de uma extensão, indicam o tipo de dados que elas contêm. A tabela a seguir lista essas extensões, juntamente com uma descrição dos dados no arquivo.



| Extensão       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none<br/> | Uma cópia completa dos dados do hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| . Alt<br/> | Uma cópia de backup do hive crítico do **\_ \_ \\ sistema de máquina local hKey** . Somente a chave do sistema tem um arquivo. Alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Um log de transações de alterações nas chaves e entradas de valor no hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| . SAV<br/> | Uma cópia de backup de um Hive.<br/> **Windows Server 2003 e Windows XP/2000:** Cópias dos arquivos do hive à medida que eles são examinados no final do estágio do modo de texto na instalação. A instalação tem dois estágios: modo de texto e modo gráfico. O hive é copiado para um arquivo. SAV após o estágio de modo de texto da instalação para protegê-lo de erros que podem ocorrer se o estágio de modo gráfico da instalação falhar. Se a instalação falhar durante o estágio de modo gráfico, somente o estágio de modo gráfico será repetido quando o computador for reiniciado; o arquivo. SAV é usado para restaurar os dados do hive.<br/> |



 

A tabela a seguir lista os hives padrão e seus arquivos de suporte.



| Hive do registro                      | Arquivos de suporte                           |
|------------------------------------|--------------------------------------------|
| **\_configuração atual de hKey \_**          | Sistema, System. Alt, System. log, System. SAV |
| **HKEY \_ Current \_ User**            | Ntuser. dat, Ntuser. dat. log                 |
| **HKEY \_ local \_ Machine \\ Sam**      | Sam, Sam. log, Sam. SAV                      |
| **HKEY \_ local \_ Machine \\ Security** | Security, Security. log, Security. SAV       |
| **HKEY \_ \_ computador local \\ software** | Software, software. log, software. SAV       |
| **HKEY \_ \_ computador local \\ System**   | Sistema, System. Alt, System. log, System. SAV |
| **usuários de HKEY \_ \\ . OS**          | Padrão, Default. log, Default. SAV          |



 

 

 




