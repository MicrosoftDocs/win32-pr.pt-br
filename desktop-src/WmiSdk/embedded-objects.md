---
description: Um objeto incorporado é um objeto de uma classe que existe dentro de uma declaração de classe ou instância de outra classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Inserindo objetos em uma classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787782"
---
# <a name="embedding-objects-in-a-class"></a>Inserindo objetos em uma classe

Um objeto incorporado é um objeto de uma classe que existe dentro de uma declaração de classe ou instância de outra classe. Por exemplo, a classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contém objetos inseridos do [**Win32 com \_ confiança**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) . Cada um dos objetos de **\_ confiança do Win32** contém um objeto do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) . O WMI não limita a profundidade para a qual uma classe pode ter objetos incorporados. No entanto, usar outro design, como a criação de uma classe de associação, pode tornar um esquema mais gerenciável.

Para obter mais informações sobre objetos inseridos, consulte os seguintes tópicos:

-   [Criando objetos inseridos](creating-embedded-objects.md)
-   [Consultando objetos inseridos](querying-embedded-objects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
