---
description: Clonagem e compartilhamento (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonagem e compartilhamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96add856c6e3c675cbf3ac225d39517214ed9dc002abded6f4f7f9f75d4736bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857696"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonagem e compartilhamento (Direct3D 9)

## <a name="cloning-parameters"></a>Clonando parâmetros

A clonagem tem as seguintes restrições.

-   Os clones herdam o pool do efeito original. Consulte a seção Parâmetros de Compartilhamento.
-   Os clones herdam técnicas, passagens, parâmetros e anotações do efeito original (incluindo todas as anotações adicionadas com [**ID3DXEffect).**](id3dxeffect.md)
-   Os clones herdam as anotações adicionadas dinamicamente do efeito original.
-   A clonagem em um novo dispositivo falhará se o pool do efeito original não for **NULL** e o efeito original contiver um parâmetro dependente de dispositivo compartilhado (como uma textura ou sombreador).

## <a name="sharing-parameters"></a>Compartilhamento de parâmetros

Um pool é um buffer que compartilha parâmetros de efeito entre diferentes efeitos. Para adicionar parâmetros a um pool, especifique um uso compartilhado quando o efeito for criado.

Um pool tem as seguintes restrições.

-   Um parâmetro é adicionado ao pool na primeira vez que um efeito que contém esse parâmetro (compartilhado) é adicionado ao pool.
-   Um pool obtém valores iniciais do primeiro parâmetro compartilhado; os parâmetros compartilhados subsequentemente obterão seus valores do pool.
-   Um parâmetro é excluído do pool quando todas as referências de efeito ao parâmetro compartilhado são liberadas.
-   Todos os efeitos no pool que contêm o mesmo parâmetro dependente do dispositivo (compartilhado) devem ter o mesmo dispositivo.

**NULL** pode ser usado para especificar nenhum pool, caso em que nenhum parâmetro é compartilhado. Isso é quase equivalente a especificar um pool exclusivo apenas para esse efeito. A única diferença é que, quando o efeito é clonado, o clone não compartilhará seus parâmetros compartilhados com o original.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



