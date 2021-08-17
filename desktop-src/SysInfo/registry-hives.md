---
description: Um hive é um grupo lógico de chaves, sub-chaves e valores no Registro que tem um conjunto de arquivos de suporte que contêm backups de seus dados.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Hives do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11920a7b70a8aeb78b08aee2c25b89c4de5457b5cb96a480fc1f75fff6c6a35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763623"
---
# <a name="registry-hives"></a>Hives do Registro

Um *hive* é um grupo lógico de chaves, sub-chaves e valores no Registro que tem um conjunto de arquivos de suporte carregados na memória quando o sistema operacional é iniciado ou um usuário faz logo login.

Sempre que um novo usuário faz login em um computador, um novo hive é criado para esse usuário com um arquivo separado para o perfil do usuário. Isso é chamado de *hive de perfil do usuário.* O hive de um usuário contém informações específicas do Registro referentes às configurações do aplicativo do usuário, área de trabalho, ambiente, conexões de rede e impressoras. Os hives de perfil do usuário estão localizados na **chave USUÁRIOS \_ do HKEY.**

Os arquivos do Registro têm os dois formatos a seguir: standard e latest. O formato padrão é o único formato com suporte Windows 2000. Também há suporte para versões posteriores do Windows para compatibilidade com versões anteriores. O formato mais recente tem suporte a partir do Windows XP. Em versões do Windows que suportam o formato mais recente, os seguintes hives ainda usam o formato padrão: **HKEY \_ CURRENT \_ USER,** **HKEY \_ LOCAL MACHINE \_ \\ SAM,** **HKEY LOCAL MACHINE \_ \_ \\ Security** e **HKEY USERS \_ \\ . DEFAULT**; todos os outros hives usam o formato mais recente.

A maioria dos arquivos de suporte para os hives está no diretório %SystemRoot% \\ System32 \\ Config. Esses arquivos são atualizados sempre que um usuário faz login. As extensões de nome de arquivo dos arquivos nesses diretórios ou, em alguns casos, uma falta de uma extensão, indicam o tipo de dados que eles contêm. A tabela a seguir lista essas extensões juntamente com uma descrição dos dados no arquivo.



| Extensão       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nenhum<br/> | Uma cópia completa dos dados do hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| .alt<br/> | Uma cópia de backup do hive crítico **do sistema HKEY \_ LOCAL \_ MACHINE. \\** Somente a chave System tem um arquivo .alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Um log de transações de alterações nas chaves e entradas de valor no hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| .sav<br/> | Uma cópia de backup de um hive.<br/> **Windows Server 2003 e Windows XP/2000:** Cópias dos arquivos do Hive conforme eles olharam para o final do estágio de modo de texto na Instalação. A instalação tem dois estágios: modo de texto e modo gráfico. O hive é copiado para um arquivo .sav após o estágio de modo de texto da instalação para protegê-lo contra erros que podem ocorrer se o estágio de modo gráfico da instalação falhar. Se a instalação falhar durante o estágio do modo gráfico, somente o estágio do modo gráfico será repetido quando o computador for reiniciado; o arquivo .sav é usado para restaurar os dados do hive.<br/> |



 

A tabela a seguir lista os hives padrão e seus arquivos de suporte.



| Hive do Registro                      | Arquivos de suporte                           |
|------------------------------------|--------------------------------------------|
| **CONFIGURAÇÃO \_ ATUAL DO HKEY \_**          | System, System.alt, System.log, System.sav |
| **USUÁRIO ATUAL DO HKEY \_ \_**            | Ntuser.dat, Ntuser.dat.log                 |
| **HKEY \_ LOCAL \_ MACHINE \\ SAM**      | Sam, Sam.log, Sam.sav                      |
| **HKEY \_ LOCAL \_ MACHINE \\ Security** | Security, Security.log, Security.sav       |
| **HKEY \_ LOCAL \_ MACHINE \\ Software** | Software, Software.log, Software.sav       |
| **Sistema de COMPUTADOR \_ LOCAL \_ HKEY \\**   | System, System.alt, System.log, System.sav |
| **USUÁRIOS HKEY \_ \\ . Padrão**          | Default, Default.log, Default.sav          |



 

 

 




