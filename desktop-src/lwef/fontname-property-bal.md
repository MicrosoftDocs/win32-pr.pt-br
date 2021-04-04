---
title: Propriedade FontName (objeto Balloon)
description: Propriedade FontName
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085090"
---
# <a name="fontname-property-balloon-object"></a>Propriedade FontName (objeto Balloon)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a fonte usada no balão de palavras para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). Fonte Balloon. NomeDaFonte_ *  \[  =  \]



| Parte   | Descrição                                      |
|--------|--------------------------------------------------|
| *la* | Um valor de cadeia de caracteres correspondente ao nome da fonte. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade [**FontName**](fontname-property.md) define a fonte usada para exibir texto na janela balão de uma cadeia de caracteres. O valor padrão das configurações de fonte do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> Se você estiver usando um caractere que não foi compilado, verifique as propriedades [**NomeDaFonte**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) do caractere para determinar se elas são apropriadas para sua localidade. Talvez seja necessário definir esses valores antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.

 

 

 




