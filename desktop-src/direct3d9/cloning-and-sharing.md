---
description: Clonagem e compartilhamento (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonagem e compartilhamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826645"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonagem e compartilhamento (Direct3D 9)

## <a name="cloning-parameters"></a>Parâmetros de clonagem

A clonagem tem as seguintes restrições.

-   Os clones herdam o pool do efeito original. Consulte a seção parâmetros de compartilhamento.
-   Os clones herdam as técnicas, passagens, parâmetros e anotações do efeito original (incluindo todas as anotações adicionadas com [**ID3DXEffect**](id3dxeffect.md)).
-   Os clones herdam as anotações adicionadas dinamicamente do efeito original.
-   A clonagem em um novo dispositivo falhará se o pool do efeito original não for **nulo** e o efeito original contivesse um parâmetro dependente de dispositivo compartilhado (como uma textura ou sombreador).

## <a name="sharing-parameters"></a>Compartilhando parâmetros

Um pool é um buffer que compartilha parâmetros de efeito entre diferentes efeitos. Para adicionar parâmetros a um pool, especifique um uso compartilhado quando o efeito for criado.

Um pool tem as seguintes restrições.

-   Um parâmetro é adicionado ao pool na primeira vez que um efeito contendo esse parâmetro (compartilhado) é adicionado ao pool.
-   Um pool obtém valores iniciais do primeiro parâmetro compartilhado; os parâmetros compartilhados subsequentemente obtêm seus valores do pool.
-   Um parâmetro é excluído do pool quando todas as referências de efeito para o parâmetro compartilhado são liberadas.
-   Todos os efeitos no pool que contêm o mesmo parâmetro dependente de dispositivo (compartilhado) devem ter o mesmo dispositivo.

**NULL** pode ser usado para especificar nenhum pool; nesse caso, nenhum parâmetro é compartilhado. Isso é quase equivalente a especificar um pool exclusivo apenas para esse efeito. A única diferença é que, quando o efeito é clonado, o clone não compartilhará seus parâmetros compartilhados com o original.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



