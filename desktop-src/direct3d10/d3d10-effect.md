---
description: Essas constantes são usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296081"
---
# <a name="d3d10_effect-constants"></a>Constantes de efeito de D3D10 \_

Essas constantes são usadas ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.



| \#definir                                 | Valor        | Descrição                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Efeito \_ \_ filho de compilação de efeitos d3d10 \_ \_    | 1 << 0 | Compile o arquivo. FX para um efeito filho. Os efeitos filho não têm inicializações para nenhum valor compartilhado porque eles são inicializados no pool de efeitos.                                                                                                           |
| D3D10 de \_ efeito de \_ compilação \_ permitir \_ operações lentas \_ | 1 << 1 | Por padrão, o modo de desempenho está habilitado. O modo de desempenho não permite objetos de estado mutável, impedindo que expressões não literais apareçam nas definições de objeto de estado. A especificação desse sinalizador desabilitará o modo e permitirá objetos de estado mutável. |
| \_Efeito de \_ d3d10 \_ thread único          | 1 << 3 | Não tente sincronizar com outros threads que carregam efeitos no mesmo pool.                                                                                                                                                                        |



 

Essas constantes são definidas como macros em d3d10effect. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



