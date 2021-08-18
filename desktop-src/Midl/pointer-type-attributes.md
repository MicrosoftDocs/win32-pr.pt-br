---
title: Atributos de tipo de ponteiro
description: Os atributos a seguir especificam as características dos ponteiros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL, atributos, tipo de ponteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8355a71428c957804596531ea428fb99a779478b677eaa2094cc4db323c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013724"
---
# <a name="pointer-type-attributes"></a>Atributos de tipo de ponteiro

Os atributos a seguir especificam as características dos ponteiros.



| Atributo                                   | Uso                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Designa um ponteiro como um ponteiro completo, com todos os recursos de um ponteiro de linguagem C, incluindo alias.                                                                                       |
| [**ref**](ref.md)                          | Designa o tipo mais simples de ponteiro em MIDL– um que simplesmente fornece o endereço de alguns dados. Ponteiros de referência nunca podem ser nulos.                                                             |
| [**Único**](unique.md)                    | Permite que um ponteiro seja nulo, mas não dá suporte ao alias.                                                                                                                                               |
| [**padrão \_ do ponteiro**](pointer-default.md) | Aplicado a uma interface para especificar o tipo de ponteiro padrão para todos os ponteiros nessa interface, exceto para ponteiros de parâmetro de nível superior, que assumem automaticamente como padrão [**os ponteiros ref.**](ref.md) |
| [**iid \_ é**](iid-is.md)                   | Fornece o identificador de interface da interface COM que é o objeto do ponteiro.                                                                                                            |
| [**string**](string.md)                    | Especifica que o ponteiro aponta para uma cadeia de caracteres.                                                                                                                                                       |



 

 

 




