---
description: MsiFiler.exe popula a tabela de arquivos com versões de arquivo, idiomas e tamanhos com base em um diretório de origem. Ele também pode atualizar a tabela MsiFileHash com hashes de arquivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754637"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe popula a [tabela de arquivos](file-table.md) com versões de arquivo, idiomas e tamanhos com base em um diretório de origem. Ele também pode atualizar a [tabela MsiFileHash](msifilehash-table.md) com hashes de arquivo.

## <a name="syntax"></a>Syntax

**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**

## <a name="command-line-options"></a>Opções de linha de comando

Msifiler.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço.



| Opção | Parâmetro   | Descrição                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | O banco de dados (arquivo. msi) a ser atualizado.                                                                                                                              |
| -v     |             | Use o modo detalhado.                                                                                                                                                            |
| -H     |             | Preencha a [tabela MsiFileHash](msifilehash-table.md). Isso criará a tabela se ela ainda não existir. A tabela MsiFileHash só pode ser usada com arquivos sem versão. |
| -S     | *ALTSOURCE* | ALTSOURCE especifica um diretório alternativo para localizar os arquivos.                                                                                                              |



 

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Usando a tabela de diretórios](using-the-directory-table.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



