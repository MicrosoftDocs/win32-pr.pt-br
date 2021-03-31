---
description: Tabelas que listam comparações de suporte a funcionalidades e recursos para os quatro principais sistemas de arquivos do Windows, NTFS, exFAT, UDF e FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Comparação de funcionalidade do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7547e48ff68a8fdab195087904a47a535aa3464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647666"
---
# <a name="file-system-functionality-comparison"></a>Comparação de funcionalidade do sistema de arquivos

As tabelas a seguir listam as comparações de suporte a recursos e funcionalidades para os quatro principais sistemas de arquivos do Windows, NTFS, exFAT, UDF e FAT32:

-   [Funcionalidade](#file-system-functionality-comparison)
-   [Limites](#limits)
-   [Registro em diário e log de alterações](#journaling-and-change-log)
-   [Bloquear recursos de alocação](#block-allocation-features)
-   [Segurança](#security)
-   [Compactação](#compression)
-   [Cotas](#quotas)
-   [Armazenamento de instância única](#single-instance-store)
-   [Tópicos relacionados](#related-topics)

## <a name="functionality"></a>Funcionalidade



| Recurso                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Carimbos de data/hora de criação<br/>     | Sim<br/>                 | Sim<br/> | Sim<br/>                | Sim<br/>             |
| Carimbos de data/hora do último acesso<br/>  | Não (consulte a observação abaixo)<br/> | Sim<br/> | Sim<br/>                | Sim (somente data)<br/> |
| Carimbos de data da última alteração<br/>  | Sim<br/>                 | Sim<br/> | Sim<br/>                | Sim<br/>             |
| Carimbos de data/hora do último arquivo<br/> | Não<br/>                  | Não<br/>  | Não<br/>                 | Não<br/>              |
| Diferenciar maiúsculas de minúsculas<br/>           | Sim (opção)<br/>        | Não<br/>  | Sim<br/>                | Não<br/>              |
| Preservação de maiúsculas e minúsculas<br/>          | Sim<br/>                 | Sim<br/> | Sim<br/>                | Sim<br/>             |
| Links físicos<br/>               | Sim<br/>                 | Não<br/>  | Sim<br/>                | Não<br/>              |
| Links virtuais<br/>               | Sim<br/>                 | Não<br/>  | Não<br/>                 | Não<br/>              |
| Arquivos esparsos<br/>             | Sim<br/>                 | Não<br/>  | Sim<br/>                | Não<br/>              |
| Fluxos nomeados<br/>            | Sim<br/>                 | Não<br/>  | Sim<br/>                | Não<br/>              |
| Oplocks<br/>                  | Sim<br/>                 | Sim<br/> | Sim<br/>                | Sim<br/>             |
| Atributos estendidos<br/>      | Sim<br/>                 | Não<br/>  | Sim (somente em disco)<br/> | Não<br/>              |
| Fluxos de dados alternativos<br/>   | Sim<br/>                 | Não<br/>  | Sim<br/>                | Não<br/>              |
| Pontos de montagem<br/>             | Sim<br/>                 | Não<br/>  | Não<br/>                 | Não<br/>              |



 

**Windows Server 2003 e Windows XP:** O campo carimbo de data/hora do último acesso ao NTFS é atualizado.

## <a name="limits"></a>Limites



| Recurso                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Tamanho máximo do nome do arquivo<br/> | 255 caracteres Unicode<br/>                                                         | 255 caracteres Unicode<br/>                                                         | 127 caracteres ASCII Unicode ou 254<br/>                                            | 255 caracteres Unicode<br/>                                                         |
| Tamanho máximo do nome do caminho<br/> | 32.760 caracteres Unicode com cada componente de caminho com até 255 caracteres<br/> | 32.760 caracteres Unicode com cada componente de caminho com até 255 caracteres<br/> | 32.760 caracteres Unicode com cada componente de caminho com até 255 caracteres<br/> | 32.760 caracteres Unicode com cada componente de caminho com até 255 caracteres<br/> |
| Tamanho máximo do arquivo<br/>        | 2 ^ 64 1 bytes<br/>                                                                   | 2 ^ 64 1 bytes<br/>                                                                   | 2 ^ 64 1 bytes<br/>                                                                   | 4 GiB<br/>                                                                          |
| Tamanho máximo do volume<br/>      | 16 TB (tamanho de cluster de 4 KB) ou 256TB (tamanho de cluster de 64 KB)<br/>                        | 2 ^ 32 1 clusters (tamanho máximo do cluster = 2 ^ 25 1)<br/>                               | 2 ^ 32 blocos<br/>                                                                    | 2 ^ 32 blocos<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Registro em diário e log de alterações



| Recurso                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Diário somente de metadados<br/> | Sim<br/> | Não<br/> | Não<br/> | Não<br/> |
| Log de alterações de arquivo<br/>          | Sim<br/> | Não<br/> | Não<br/> | Não<br/> |



 

## <a name="block-allocation-features"></a>Bloquear recursos de alocação



| Recurso                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Embalagem da parte final<br/>        | Sim (arquivos pequenos são tornados residentes no descritor de fluxo de MFT)<br/> | Não<br/> | Não<br/>  | Não<br/> |
| Extensões<br/>             | Sim<br/>                                                              | Não<br/> | Sim<br/> | Não<br/> |
| Tamanho do bloco variável<br/> | Não (definido pelo volume)<br/>                                           | Não<br/> | Não<br/>  | Não<br/> |



 

## <a name="security"></a>Segurança



| Recurso                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Acompanhar proprietário do arquivo<br/>              | Sim<br/>                                       | Não<br/>       | Não<br/>       | Não<br/> |
| Permissões de arquivo POSIX<br/>        | Não (disponível no recurso de subsistema POSIX)<br/> | Não<br/>       | Sim<br/>      | Não<br/> |
| Listas de controle de acesso<br/>          | Sim<br/>                                       | Não<br/>       | Não<br/>       | Não<br/> |
| Criptografia no nível do sistema de arquivos<br/> | Sim<br/>                                       | Não<br/>       | Não<br/>       | Não<br/> |
| Soma de verificação/ECC<br/>                  | Não<br/>                                        | Metadados<br/> | Metadados<br/> | Não<br/> |



 

## <a name="compression"></a>Compactação



| Recurso                         | NTFS           | exFAT         | UDF           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Compactação interna<br/> | Sim<br/> | Não<br/> | Não<br/> | Não<br/> |



 

## <a name="quotas"></a>Cotas



| Recurso                               | NTFS                           | exFAT         | UDF           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Espaço em disco no nível do usuário<br/>      | Sim<br/>                 | Não<br/> | Não<br/> | Não<br/> |
| Espaço em disco no nível de diretório<br/> | Não (consulte a observação abaixo)<br/> | Não<br/> | Não<br/> | Não<br/> |



 

**Observação**  O recurso cotas de espaço em disco no nível de diretório no NTFS está disponível por meio do Gerenciador de recursos do servidor de arquivos.

## <a name="single-instance-store"></a>Single-Instance Store



| Recurso               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| Nível de arquivo<br/> | Não (consulte a observação abaixo)<br/> | Não<br/> | Não<br/> | Não<br/> |



 

**Observação**  O repositório de instância única para NTFS está disponível como parte do recurso de armazenamento de instância única no Windows Server.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de arquivos](about-file-management.md)
</dt> <dt>

[Armazenamento de instância única e backup do SIS](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 

