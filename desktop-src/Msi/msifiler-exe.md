---
description: MsiFiler.exe preenche a tabela Arquivo com versões de arquivo, idiomas e tamanhos com base em um diretório de origem. Ele também pode atualizar a tabela MsiFileHash com hashes de arquivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d3306fdae929c3659baf07668486fdf8a828012ce3142e4285bde8ad7a6c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679636"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe preenche a tabela [Arquivo com](file-table.md) versões de arquivo, idiomas e tamanhos com base em um diretório de origem. Ele também pode atualizar a [tabela MsiFileHash com](msifilehash-table.md) hashes de arquivo.

## <a name="syntax"></a>Syntax

**msifiler.exe -d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**

## <a name="command-line-options"></a>Opções de linha de comando

Msifiler.exe usa as seguintes opções de linha de comando sem valor de maiúsculas e minúsculas. Um delimiter de barra também pode ser usado no lugar de um traço.



| Opção | Parâmetro   | Descrição                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | O banco de dados (.msi arquivo) que deve ser atualizado.                                                                                                                              |
| -v     |             | Use o modo detalhado.                                                                                                                                                            |
| -H     |             | Preencha a [tabela MsiFileHash](msifilehash-table.md). Isso criará a tabela se ela ainda não existir. A tabela MsiFileHash só pode ser usada com arquivos sem versão. |
| -S     | *ALTSOURCE* | ALTSOURCE especifica um diretório alternativo para encontrar os arquivos.                                                                                                              |



 

Essa ferramenta só está disponível nos componentes [do SDK Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Usando a tabela de diretório](using-the-directory-table.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



