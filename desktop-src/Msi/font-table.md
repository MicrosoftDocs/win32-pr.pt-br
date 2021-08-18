---
description: A tabela Fonte contém as informações para registrar arquivos de fonte com o sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabela de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65efb786d4379bbe14fec0239cd8f3edee50f1b79a6413904b6e00331bc49a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946977"
---
# <a name="font-table"></a>Tabela de fontes

A tabela Fonte contém as informações para registrar arquivos de fonte com o sistema.

A tabela Fonte tem as seguintes colunas.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Arquivo\_    | [Identificador](identifier.md) | Y   | N        |
| FontTitle | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Arquivo\_
</dt> <dd>

Chave externa na entrada [Tabela de arquivos](file-table.md) para o arquivo de fonte. É recomendável que o componente que contém o arquivo de fonte tenha o FontsFolder especificado na coluna Diretório \_ da [tabela Componente](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nome da fonte. É recomendável que você deixe essa coluna nula para Fontes TrueType e Coleções TrueType porque o instalador pode registrar a fonte depois de ler o título correto da fonte do arquivo de fonte. Se o nome da fonte for inserido, ele deverá ser idêntico ao título da fonte do arquivo de fonte. Você deve especificar um título para fontes que não têm nomes inseridos, como arquivos .fon.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referenciada quando a [ação RegisterFonts ou](registerfonts-action.md) [a ação UnregisterFonts](unregisterfonts-action.md) é executada.

Se o campo FontTitle for deixado nulo, o Nome da fonte será lido diretamente do arquivo de fonte especificado. Se o nome da fonte registrado no campo FontTitle for diferente do nome da fonte interna registrado no arquivo de fonte, a fonte será registrada duas vezes pela [ação RegisterFonts](registerfonts-action.md).

Os arquivos de fonte não devem ser autorados com uma ID de idioma, pois as fontes não têm um recurso de ID de idioma inserido. Portanto, a coluna Idioma da [tabela Arquivo deve](file-table.md) ser deixada nula para arquivos de fonte.

Como o instalador não refcounta arquivos de fonte por padrão, arquivos de fonte preexistentes podem ser removidos com seu componente ao desinstalar um aplicativo. Para garantir que um arquivo de fonte não seja removido, os autores podem definir os sinalizadores de bit **msidbComponentAttributesSharedDllRefCount** ou **msidbComponentAttributesPermanent** bit flags na coluna Attributes da Tabela de \_ Componentes msi Component Table para o componente que contém o arquivo de \_ \_ fonte.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



