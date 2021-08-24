---
title: Atributo ShadowFilePath
description: O atributo ShadowFilePath é o caminho totalmente qualificado para um arquivo de sombra.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Windows Media Player de atributo ShadowFilePath
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf1e8f2eb5cb810004ea219aac62973377111902071beb78eca051df19877f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002146"
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

 

 





