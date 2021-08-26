---
description: a tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar Windows proteção de arquivo quando os arquivos são instalados no Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabela MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d233f09aa62b5f6d17112b1f5a98753e328f3a1746c452de5a5a1689a36f971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042666"
---
# <a name="msisfcbypass-table"></a>Tabela MsiSFCBypass

a tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar Windows proteção de arquivo quando os arquivos são instalados no Microsoft Windows Me.

A tabela MsiSFCBypass tem a seguinte coluna.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Arquivo\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

a chave estrangeira para a [tabela de arquivos](file-table.md) que especifica o arquivo que deve ignorar Windows proteção de arquivo quando o arquivo é instalado no Windows Me.

</dd> </dl>

 

 



