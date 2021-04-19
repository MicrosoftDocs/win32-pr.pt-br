---
title: Método play (recursos de ambiente herdado do Windows)
description: Método play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105813225"
---
# <a name="play-method-legacy-windows-environment-features"></a>Método play (recursos de ambiente herdado do Windows)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Reproduz a animação especificada para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Reproduzir_* "*animationname*"

</dd> </dl> 

| Parte            | Descrição                                                          |
|-----------------|----------------------------------------------------------------------|
| *Animaçãoname* | Obrigatórios. Uma cadeia de caracteres que especifica o nome de uma sequência de animação. |



 

## <a name="remarks"></a>Comentários

O nome de uma animação é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent. Antes de reproduzir a animação especificada, o servidor tentará reproduzir a animação de **retorno** para a animação anterior, se uma tiver sido atribuída.

Ao acessar as animações de um caractere usando um protocolo de arquivo convencional, você pode simplesmente usar o método **Play** especificando o nome da animação. No entanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método **Get** para carregar a animação antes de chamar o método **Play** .

Para obter mais informações, consulte o método **Get** .

Para simplificar a sintaxe, você pode declarar uma referência de objeto e defini-la para fazer referência ao objeto [**Character**](/windows/desktop/lwef/the-characters-object) na coleção [**Characters**](/windows/desktop/lwef/the-characters-object) e usar a referência como parte de suas instruções **Play** :


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se você especificar uma animação que não está carregada ou se o caractere não tiver sido carregado com êxito, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. No entanto, se a animação não existir e os dados do caractere já tiverem sido carregados com êxito, o servidor gerará um erro.

O método **Play** não torna o caractere visível. Se o caractere não estiver visível, o servidor reproduzirá a animação de forma invisível e definirá a propriedade [**status**](status-property.md) do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

 

 
