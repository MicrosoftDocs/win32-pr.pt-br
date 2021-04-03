---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Proteção de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837257"
---
# <a name="depnx-protection"></a>Proteção de DEP/NX

A partir do Windows Internet Explorer 7 no Windows Vista, o item do painel de controle da Internet inclui uma opção **habilitar proteção de memória** para ajudar a mitigar os ataques online. Essa opção também é conhecida como DEP ( *prevenção de execução de dados* ) ou *não executar* (NX). Quando essa opção está habilitada, ela funciona com o processador para ajudar a evitar ataques de estouro de buffer bloqueando a execução de código da memória marcada como não executável.

No Windows Internet Explorer 8 no sistema operacional Windows Vista com Service Pack 1 (SP1) ou em uma versão posterior, essa opção é habilitada por padrão. O DEP/NX não protege contra todas as vulnerabilidades baseadas em memória. Mas quando ele é combinado com outras tecnologias como o ASLR (Address Space layout Randomization), ele ajuda a evitar vulnerabilidades de estouro de buffer comuns no Windows Internet Explorer e os complementos que ele carrega. Nenhuma interação adicional do usuário é necessária para fornecer essa proteção, e nenhum prompt novo é introduzido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



