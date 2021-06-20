---
title: Propriedade Enabled (objeto AudioOutput)
description: Saiba mais sobre a propriedade de objeto AudioOutput habilitada. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407339"
---
# <a name="enabled-property-audiooutput-object"></a>Propriedade Enabled (objeto AudioOutput)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor booleano que indica se a saída de áudio (falada) está habilitada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent * * *. AudioOutput. Enabled**



| Valor     | Descrição                               |
|-----------|-------------------------------------------|
| **Verdadeiro**  | Os A saída de áudio falada está habilitada. |
| **Falso** | A saída de áudio falada está desabilitada.          |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade reflete a opção reproduzir saída de áudio na página saída da folha de propriedades do agente (opções avançadas de caractere). Quando a propriedade [**Enabled**](enabled-property.md) retornar **true**, o método [**Speak**](speak-method.md) produzirá a saída de áudio se um mecanismo de TTS compatível estiver instalado ou se você usar arquivos de som para saída falada. Quando retorna **false**, isso significa que a saída de fala não está instalada ou foi desabilitada pelo usuário. A configuração de propriedade aplica-se a todos os caracteres do agente e é somente leitura; somente o usuário pode definir esse valor de propriedade.

## <a name="see-also"></a>Consulte Também

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 




