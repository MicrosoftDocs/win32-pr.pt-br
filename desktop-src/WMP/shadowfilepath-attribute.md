---
title: Atributo ShadowFilePath
description: O atributo ShadowFilePath é o caminho totalmente qualificado para um arquivo de sombra.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Atributo ShadowFilePath Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747714"
---
# <a name="shadowfilepath-attribute"></a>Atributo ShadowFilePath

O atributo **ShadowFilePath** é o caminho totalmente qualificado para um arquivo de sombra.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)

## <a name="remarks"></a>Comentários

Um *arquivo de sombra* é criado como parte de uma conversão de formato de arquivo. É a cópia de um arquivo que o Player usa quando o usuário sincroniza o conteúdo do computador para um dispositivo que exige que o conteúdo esteja no formato de arquivo original. Esse atributo é definido para o arquivo convertido a fim de apontar para o local do arquivo de sombra.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sobre o processo de conversão**](about-the-conversion-process.md)
</dt> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





