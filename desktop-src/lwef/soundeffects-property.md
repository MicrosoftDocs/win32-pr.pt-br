---
title: Propriedade SoundEffects
description: Propriedade SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3894782ec3a038831f7bab7d6d5fe0701936baf1c1add136ad5c2c3446f78867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246252"
---
# <a name="soundeffects-property"></a>Propriedade SoundEffects

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna um booliana que indica se os efeitos de som (. WAV) arquivos configurados como parte das ações de um caractere serão reproduzir.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. AudioOutput.SoundEffects**



| Valor     | Descrição                          |
|-----------|--------------------------------------|
| **Verdadeiro**  | Os efeitos de som de caractere estão habilitados. |
| **Falso** | O efeito de som do caractere está desabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade reflete a opção Reproduzir Efeitos de Som de Caractere na página Saída da folha de propriedades do Agent (Opções De Caracteres Avançadas). Quando a **propriedade SoundEffects** retornar **True,** os efeitos de som incluídos na definição de um caractere serão interpretados. Quando **False**, os efeitos de som não serão interpretados. A configuração de propriedade afeta todos os caracteres e é somente leitura; somente o usuário pode definir esse valor da propriedade.

## <a name="see-also"></a>Consulte Também

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




