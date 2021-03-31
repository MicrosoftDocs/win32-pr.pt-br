---
description: A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto. Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabela PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172010"
---
# <a name="patchpackage-table"></a>Tabela PatchPackage

A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto. Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.

A tabela PatchPackage tem as colunas a seguir.



| Coluna  | Tipo                   | Chave | Nullable |
|---------|------------------------|-----|----------|
| PatchID | [GUID](guid.md)       | S   | N        |
| Mídia\_ | [Inteiro](integer.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchID
</dt> <dd>

Esta coluna contém um identificador exclusivo para esse patch específico.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Meio\_
</dt> <dd>

Esta coluna é uma chave estrangeira para a coluna DiskId da [tabela de mídia](media-table.md) e indica o disco que contém o pacote de patch.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela PatchPackage é necessária em cada pacote de patch. Se a tabela estiver ausente, as tentativas de instalar o patch falharão com "erro 2768: a transformação no pacote de patch é inválida." Normalmente, essa tabela é adicionada ao pacote de instalação por uma transformação de um pacote de patch. Normalmente, ele não é criado diretamente em um pacote de instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



