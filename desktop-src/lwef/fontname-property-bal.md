---
title: Propriedade FontName (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto Balão FontName. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068262"
---
# <a name="fontname-property-balloon-object"></a>Propriedade FontName (objeto Balloon)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a fonte usada no balão de palavras para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Fonte Balloon.FontName_ *  \[  =  \]



| Parte   | Descrição                                      |
|--------|--------------------------------------------------|
| *Fonte* | Um valor de cadeia de caracteres correspondente ao nome da fonte. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**propriedade FontName**](fontname-property.md) define a fonte usada para exibir texto na janela de balão de palavra de uma cadeia de caracteres. O valor padrão para as configurações de fonte do balão de palavra de um caractere é definido no Editor de Caracteres do Microsoft Agent. Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> Se você estiver usando um caractere que não compilou, verifique as propriedades [**FontName**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) do caractere para determinar se elas são apropriadas para sua localidade. Talvez seja necessário definir esses valores antes de usar o [**método Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.

 

 

 




