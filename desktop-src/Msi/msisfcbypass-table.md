---
description: A tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar a proteção de arquivos do Windows quando os arquivos são instalados no Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabela MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297116"
---
# <a name="msisfcbypass-table"></a>Tabela MsiSFCBypass

A tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar a proteção de arquivos do Windows quando os arquivos são instalados no Microsoft Windows me.

A tabela MsiSFCBypass tem a seguinte coluna.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Arquivo\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

A chave estrangeira para a [tabela de arquivos](file-table.md) que especifica o arquivo que deve ignorar a proteção de arquivos do Windows quando o arquivo é instalado no Windows me.

</dd> </dl>

 

 



