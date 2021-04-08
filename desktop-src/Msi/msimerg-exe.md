---
description: Msimerg.exe é um utilitário de linha de comando que usa MsiDatabaseMerge para mesclar um banco de dados de referência em um banco de dados base.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922540"
---
# <a name="msimergexe"></a>Msimerg.exe

Msimerg.exe é um utilitário de linha de comando que usa [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para [mesclar](merges-and-transforms.md) um banco de dados de referência em um banco de dados base.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntax

**Msimerg** *{banco de dados base} {Reference Database}*

Se houver um conflito de mesclagem entre os dois bancos de dados, as informações de conflito serão colocadas na \_ tabela MergeErrors.

## <a name="command-line-options"></a>Opções de linha de comando

Nenhum.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



