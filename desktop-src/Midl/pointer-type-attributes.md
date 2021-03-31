---
title: Atributos de tipo de ponteiro
description: Os atributos a seguir especificam as características dos ponteiros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL, atributos, tipo de ponteiro de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637187"
---
# <a name="pointer-type-attributes"></a>Atributos de tipo de ponteiro

Os atributos a seguir especificam as características dos ponteiros.



| Atributo                                   | Uso                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Designa um ponteiro como um ponteiro completo, com todos os recursos de um ponteiro de linguagem C, incluindo alias.                                                                                       |
| [**ref**](ref.md)                          | Designa o tipo mais simples de ponteiro no MIDL — um que simplesmente fornece o endereço de alguns dados. Ponteiros de referência nunca podem ser nulos.                                                             |
| [**diferente**](unique.md)                    | Permite que um ponteiro seja nulo, mas não oferece suporte a aliases.                                                                                                                                               |
| [**padrão de ponteiro \_**](pointer-default.md) | Aplicado a uma interface para especificar o tipo de ponteiro padrão para todos os ponteiros nessa interface, exceto para ponteiros de parâmetro de nível superior, que são automaticamente padronizados para ponteiros de [**referência**](ref.md) . |
| [**IID \_ é**](iid-is.md)                   | Fornece o identificador de interface da interface COM que é o objeto do ponteiro.                                                                                                            |
| [**string**](string.md)                    | Especifica que o ponteiro aponta para uma cadeia de caracteres.                                                                                                                                                       |



 

 

 




