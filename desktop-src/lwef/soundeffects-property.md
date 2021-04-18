---
title: Propriedade SoundEffects
description: Propriedade SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791360"
---
# <a name="soundeffects-property"></a>Propriedade SoundEffects

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor booleano que indica se os efeitos de som (. WAV) os arquivos configurados como parte das ações de um caractere serão reproduzidos.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent * * *. AudioOutput.SoundEffects**



| Valor     | Descrição                          |
|-----------|--------------------------------------|
| **Verdadeiro**  | Os efeitos de som de caractere estão habilitados. |
| **Falso** | O efeito de som de caractere está desabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade reflete a opção de efeitos sonoros de caractere de reprodução na página saída da folha de propriedades do agente (opções avançadas de caractere). Quando a propriedade **SoundEffects** retorna **true**, os efeitos sonoros incluídos na definição de um caractere serão reproduzidos. Quando **for falso**, os efeitos sonoros não serão reproduzidos. A configuração da propriedade afeta todos os caracteres e é somente leitura; somente o usuário pode definir esse valor de propriedade.

## <a name="see-also"></a>Consulte Também

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




