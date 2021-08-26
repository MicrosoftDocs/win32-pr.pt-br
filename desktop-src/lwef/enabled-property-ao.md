---
title: Propriedade Enabled (objeto AudioOutput)
description: Saiba mais sobre a propriedade de objeto Enabled AudioOutput. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 515b7148acf65d98b0ec8b5a5f324e5bfd9dccd10c874e165adfa2d0de9442ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963036"
---
# <a name="enabled-property-audiooutput-object"></a>Propriedade Enabled (objeto AudioOutput)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna um booliana que indica se a saída de áudio (falada) está habilitada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. AudioOutput.Enabled**



| Valor     | Descrição                               |
|-----------|-------------------------------------------|
| **Verdadeiro**  | (Padrão) A saída de áudio falada está habilitada. |
| **Falso** | A saída de áudio falada está desabilitada.          |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade reflete a opção Reproduzir Saída de Áudio na página Saída da folha de propriedades do Agent (Opções de Caracteres Avançadas). Quando a [**propriedade Enabled**](enabled-property.md) retornar **True**, o método [**Speak**](speak-method.md) produzirá a saída de áudio se um mecanismo TTS compatível estiver instalado ou se você usar arquivos de som para a saída falada. Quando retorna **False**, significa que a saída de fala não está instalada ou foi desabilitada pelo usuário. A configuração de propriedade se aplica a todos os caracteres do Agent e é somente leitura; somente o usuário pode definir esse valor da propriedade.

## <a name="see-also"></a>Consulte Também

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 




