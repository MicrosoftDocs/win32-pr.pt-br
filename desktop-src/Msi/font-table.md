---
description: A tabela de fontes contém as informações para o registro de arquivos de fonte com o sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabela de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922036"
---
# <a name="font-table"></a>Tabela de fontes

A tabela de fontes contém as informações para o registro de arquivos de fonte com o sistema.

A tabela de fontes tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Arquivo\_    | [Identificador](identifier.md) | S   | N        |
| FontTitle | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Chave externa na entrada da [tabela de arquivos](file-table.md) para o arquivo de fonte. É recomendável que o componente que contém o arquivo de fonte tenha o FontsFolder especificado na \_ coluna Directory da [tabela Component](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nome da fonte. É recomendável deixar essa coluna nula para fontes TrueType e coleções TrueType porque o instalador pode registrar a fonte depois de ler o título de fonte correto do arquivo de fonte. Se o nome da fonte for inserido, ele deverá ser idêntico ao título da fonte do arquivo de fonte. Você deve especificar um título para fontes que não têm nomes inseridos, como arquivos. Fon.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [RegisterFonts](registerfonts-action.md) ou a [ação UnregisterFonts](unregisterfonts-action.md) é executada.

Se o campo FontTitle for deixado nulo, o nome da fonte será lido diretamente do arquivo de fonte especificado. Se o nome da fonte registrado no campo FontTitle for diferente do nome da fonte interna registrada no arquivo de fonte, a fonte será registrada duas vezes pela [ação RegisterFonts](registerfonts-action.md).

Os arquivos de fonte não devem ser criados com uma ID de idioma, pois as fontes não têm um recurso de ID de idioma inserido. Portanto, a coluna de idioma da [tabela de arquivos](file-table.md) deve ser deixada como nula para os arquivos de fonte.

Como o instalador não concede arquivos de fonte por padrão, arquivos de fonte preexistentes podem ser removidos com seu componente ao desinstalar um aplicativo. Para garantir que um arquivo de fonte não seja removido, os autores podem definir os sinalizadores de bits **msidbComponentAttributesSharedDllRefCount** ou **MsidbComponentAttributesPermanent** na coluna atributos da tabela componente MSI de tabela de componentes \_ \_ \_ para o componente que contém o arquivo de fonte.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



