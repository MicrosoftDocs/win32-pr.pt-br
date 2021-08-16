---
title: Classes auxiliares dinâmicas
description: Semelhante às classes de objeto estrutural e abstrato, as classes auxiliares são definidas por um objeto classSchema no esquema de Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares dinâmicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce88f525b5d72a271aab1746a0ce0d0b308cb7022c4702433b82038c101435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429896"
---
# <a name="dynamic-auxiliary-classes"></a>Classes auxiliares dinâmicas

Semelhante às classes de objeto estrutural e abstrato, as classes auxiliares são definidas por um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no esquema de Active Directory. Para obter mais informações, consulte [classes estruturais, abstratas e auxiliares](structural-abstract-and-auxiliary-classes.md). Essa definição de esquema especifica várias características da classe, incluindo os atributos associados à classe.

Ao contrário das classes estruturais, não é possível criar uma instância de uma classe auxiliar como você pode com uma classe estrutural. Em vez disso, você usa uma classe auxiliar para estender a lista de atributos que está associada a outra classe de objeto estrutural, abstrata ou auxiliar.

na versão inicial do Windows 2000, Active Directory Domain Services fornecia suporte para vinculação estática de classes auxiliares à definição [**classSchema**](/windows/desktop/ADSchema/c-classschema) de outra classe de objeto. Quando uma classe auxiliar é usada dessa forma, cada instância da classe de objeto dá suporte aos atributos da classe auxiliar.

**Windows servidor 2000 e anterior:** O Active Directory Domain Services não oferece suporte para a vinculação dinâmica de classes auxiliares a objetos individuais, e não apenas a classes inteiras de objetos. Além disso, as classes auxiliares que foram anexadas a uma instância de objeto não podem ser removidas subsequentemente da instância.

**Windows Server 2003:** as Classes auxiliares dinâmicas têm suporte quando todos os controladores de domínio na floresta estão em execução Windows server 2003 e o modo funcional da floresta é Windows server 2003.

Para obter mais informações sobre as classes auxiliares, consulte:

-   [Classes auxiliares vinculadas dinamicamente](dynamically-linked-auxiliary-classes.md)
-   [Classes auxiliares vinculadas estaticamente](statically-linked-auxiliary-classes.md)
-   [Determinando as classes associadas a uma instância de objeto](determining-the-classes-associated-with-an-object-instance.md)
-   [Adicionando uma classe auxiliar a uma instância de objeto](adding-an-auxiliary-class-to-an-object-instance.md)

Para obter mais informações sobre os níveis funcionais de floresta, consulte "como aumentar Active Directory níveis funcionais de domínio e floresta" na base de dados de conhecimento de ajuda e suporte em [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 