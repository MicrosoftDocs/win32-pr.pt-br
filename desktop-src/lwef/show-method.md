---
title: Mostrar Método
description: Mostrar Método
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede9dd8474b21911fccb0c217b070dbfb84160125d2fd56092685ccaf82905b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475348"
---
# <a name="show-method"></a>Mostrar Método

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Torna o caractere especificado visível e reproduz sua animação **De exibição** associada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Mostrar_ *  \[ *Rápido*\]



| Parte   | Descrição                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Uma expressão booliana que especifica se o servidor reproduz a **animação Mostrando.** **True** Ignora a **animação Mostrando** estado. <br/> **False** (Padrão) Não ignora a **animação de** estado Mostrando. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Além disso, se  a animação Showing associada não tiver sido carregada e você não  tiver especificado o parâmetro **Fast** como **True**, o servidor define a propriedade [**Status**](status-property.md) do objeto Request como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados  de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação de estado Mostrando antes de chamar o **método Show.**

Evite definir o **parâmetro Fast** como **True sem** primeiro tocar uma animação com antecedência; caso contrário, o quadro de caracteres poderá ser exibido sem imagem. Em particular, observe que, se você chamar [**MoveTo**](moveto-method.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação. Portanto, se você chamar o **método Show** com **Fast** definido como **True,** nenhuma imagem será exibida. Da mesma forma, se você chamar [**Ocultar,**](hide-method.md) **Mostrar** com **Fast** definido como **True,** não haverá nenhuma imagem visível.

## <a name="see-also"></a>Consulte Também

[**Método Hide**](hide-method.md)


 

