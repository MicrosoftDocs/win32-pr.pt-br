---
description: A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto. Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabela PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4027913854436072330a69a788ca9dc9b1365a71b82fd1727227e33d8a203b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926116"
---
# <a name="patchpackage-table"></a>Tabela PatchPackage

A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto. Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.

A tabela PatchPackage tem as colunas a seguir.



| Coluna  | Tipo                   | Chave | Nullable |
|---------|------------------------|-----|----------|
| PatchID | [GUID](guid.md)       | Y   | N        |
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

 

 



