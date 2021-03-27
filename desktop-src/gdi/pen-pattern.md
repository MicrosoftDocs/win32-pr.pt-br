---
description: O atributo Pattern especifica o padrão de uma caneta geométrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Padrão de caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502404"
---
# <a name="pen-pattern"></a>Padrão de caneta

O atributo Pattern especifica o padrão de uma caneta geométrica.

A ilustração a seguir mostra linhas desenhadas com canetas geométricas diferentes. Cada caneta foi criada usando um atributo de padrão diferente.

![ilustração mostrando quatro linhas, cada uma preenchida com uma caneta diferente](images/cspen-02.png)

A primeira linha da ilustração anterior é desenhada usando um dos seis padrões de hachura disponíveis; para obter mais informações sobre padrões de hachura, consulte [hachura](pen-hatch.md). A próxima linha é desenhada usando o padrão vazio, idêntico ao padrão NULL. A terceira linha é desenhada usando um padrão personalizado criado a partir de um bitmap de 8 por 8 pixels. (Para obter mais informações sobre bitmaps e sua criação, consulte [bitmaps](bitmaps.md).) A última linha é desenhada usando um padrão sólido. Criar um pincel e passar seu identificador para a função [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) cria um padrão.

 

 



