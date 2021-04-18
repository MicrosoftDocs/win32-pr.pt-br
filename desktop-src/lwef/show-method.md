---
title: Mostrar método
description: Mostrar método
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105760604"
---
# <a name="show-method"></a>Mostrar método

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Torna o caractere especificado visível e executa sua animação de **exibição** associada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Mostrar* *  \[ *rápido*\]



| Parte   | Descrição                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Uma expressão booliana que especifica se o servidor reproduz a animação em **exibição** . **Verdadeiro** Ignora a animação de estado de **exibição** . <br/> **False** (padrão) não ignora a animação de estado de **exibição** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se a animação de **exibição** associada não tiver sido carregada e você não tiver especificado o parâmetro **Fast** como **true**, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação de estado de **exibição** antes de chamar o método **show** .

Evite definir o parâmetro **Fast** como **true** sem primeiro reproduzir uma animação antes; caso contrário, o quadro de caracteres poderá ser exibido sem imagem. Em particular, observe que, se você chamar [**MoveTo**](moveto-method.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação. Portanto, se você chamar o método **show** com **Fast** definido como **true**, nenhuma imagem será exibida. Da mesma forma, se você chamar [**Hide**](hide-method.md) e **Mostrar** with **Fast** Set como **true**, não haverá imagem visível.

## <a name="see-also"></a>Consulte Também

[**Método Hide**](hide-method.md)


 

